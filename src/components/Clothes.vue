<template>
    <div class="ClothesBox" id="ClothesBox">
        <div class="SetClothesBox" id="SetClothesBox">
            <div class="ClothesBoxItem">
                <div class="ClothesBoxClumns_2">
                    <div>Select Sex</div>
                    <div id="SkinGender">{{ Gender }}</div>
                </div>
                <div class="ClothesBoxClumns_2 ClothesBoxClumns_SexBTN" v-if="Gender == 'Male'">
                    <div id="ClothesMaleBTN" class="ClothesSexBTN ClothesSexBTNActive" @click="ChangeSex('male')">Male
                    </div>
                    <div id="ClothesFemaleBTN" class="ClothesSexBTN" @click="ChangeSex('female')">Female</div>
                </div>
                <div class="ClothesBoxClumns_2 ClothesBoxClumns_SexBTN" v-if="Gender == 'Female'">
                    <div id="ClothesMaleBTN" class="ClothesSexBTN" @click="ChangeSex('male')">Male
                    </div>
                    <div id="ClothesFemaleBTN" class="ClothesSexBTN ClothesSexBTNActive" @click="ChangeSex('female')">
                        Female</div>
                </div>
                <div class="ClothesBoxClumns_1 MarginTop10px">
                    <div>Suggestion</div>
                </div>
                <div class="ClothesBoxClumns_6">
                    <div class="ClothesBox_BTN" id="SelectSuggestionID1" @click="SelectSuggestion(1)">1</div>
                    <div class="ClothesBox_BTN" id="SelectSuggestionID2" @click="SelectSuggestion(2)">2</div>
                    <div class="ClothesBox_BTN" id="SelectSuggestionID3" @click="SelectSuggestion(3)">3</div>
                    <div class="ClothesBox_BTN" id="SelectSuggestionID4" @click="SelectSuggestion(4)">4</div>
                    <div class="ClothesBox_BTN" id="SelectSuggestionID5" @click="SelectSuggestion(5)">5</div>
                    <div class="ClothesBox_BTN" id="SelectSuggestionID6" @click="SelectSuggestion(6)">6</div>
                </div>
            </div>




            <div v-for="(ClothesUtil, index) in ClothesUtils" :key="ClothesUtil[0]">
                <div class="ClothesBoxItem">
                    <div class="ClothesBoxClumns_2">
                        <div>{{ ClothesUtil[0] }}</div>
                        <div class="ClothesIndexAndLengh"><span :id="'ClothesShowItemValueID' + index">1</span><span> |
                            </span><span :id="'ClothesMaximumItemValueID' + index">{{
                            ClothesUtil[1]
                            }}</span></div>
                    </div>

                    <div class="ClothesBoxClumns_3 MarginTop10px">
                        <div class="ClothesBox_RBTN" :id="'LeftBTNClothesID' + (index + 1)"
                            @click="ChangeItemValue(false, index, index + 1)">&#10094;</div>
                        <input type="number" class="ClothesItemValue" :id="'ClothesItemValueID' + index"
                            @blur="CheckValueForChange(index)" @keydown='ResetElem(index)'
                            @change="ChangeClothesItemValue(index)" value="1" />
                        <div class="ClothesBox_RBTN" :id="'RightBTNClothesID' + (index + 1)"
                            @click="ChangeItemValue(true, index, index + 1)">&#10095;</div>
                    </div>
                </div>
            </div>
        </div>
        <div class="ClothesButtonBox">
            <div class="SubClothesBox">
                <div class="SubClothesButtonBox" @click="CloseBTNClicked()">Close</div>
                <div class="SubClothesButtonBox" @click="OrderBTNClicked()">Order</div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ClothesVue',
    data() {
        return {
            SelectedStatus: -1,
            Gender: '',
            ClothesUtils: [],
            eventNames: {
                clientWEB: {
                    OpenClothes: "ClientWEB:Clothes:OpenClothes",
                    SexChanged: "ClientWEB:Clothes:SexChanged",
                    KeyRowUpPressed: "ClientWEB:clothes:KeyRowUpPressed",
                    KeyRowLeftPressed: "ClientWEB:clothes:KeyRowLeftPressed",
                    SetSuggestion: 'ClientWEB:clothes:SetSuggestion',
                    close: "ClientWEB:ClothesWebView:close",
                    SetDrawableIndex: "ClientWEB:clothes:SetDrawableIndex",
                },
                WEBclient: {
                    ChangeClothes: "WEBclient:Clothes:ChangeClothes",
                    ChangeSex: "WEBclient:Clothes:ChangeSex",
                    CloseClothes: "WEBclient:Clothes:CloseClothes",
                    Suggestion: "WEBclient:Clothes:Suggestion",
                    OrderList: "WEBclient:Clothes:OrderList",
                },
            }
        }
    },
    unmounted() {
        if ("alt" in window) {
            alt.off(this.eventNames.clientWEB.OpenClothes, this.ClothesBoxOpenFromClient);
            alt.off(this.eventNames.clientWEB.SexChanged, this.ClothesBoxSexChangedFromClient);
            alt.off(this.eventNames.clientWEB.KeyRowUpPressed, this.KeyRowPressed);
            alt.off(this.eventNames.clientWEB.KeyRowLeftPressed, this.KeyRowLeftPressed);
            alt.off(this.eventNames.clientWEB.SetSuggestion, this.SetClassActiveToSuggestion);
            alt.off(this.eventNames.clientWEB.SetDrawableIndex, this.SetDrawableIndex);
            alt.off(this.eventNames.clientWEB.close, this.ClothesBoxCloseFromClient);
        }
    },
    mounted() {
        if ("alt" in window) {
            alt.on(this.eventNames.clientWEB.OpenClothes, this.ClothesBoxOpenFromClient);
            alt.on(this.eventNames.clientWEB.SexChanged, this.ClothesBoxSexChangedFromClient);
            alt.on(this.eventNames.clientWEB.KeyRowUpPressed, this.KeyRowPressed);
            alt.on(this.eventNames.clientWEB.KeyRowLeftPressed, this.KeyRowLeftPressed);
            alt.on(this.eventNames.clientWEB.SetSuggestion, this.SetClassActiveToSuggestion);
            alt.on(this.eventNames.clientWEB.SetDrawableIndex, this.SetDrawableIndex);
            alt.on(this.eventNames.clientWEB.close, this.ClothesBoxCloseFromClient);
        }
    },
    methods: {
        SetDrawableIndex(BoxComponentIndex, DrawableIndex) {
            document.getElementById('ClothesItemValueID' + BoxComponentIndex).value = DrawableIndex;
            this.ChangeClothesItemValue(BoxComponentIndex);
        },
        ClothesBoxOpenFromClient(Gender, ClothesUtils) {
            this.AddClothesItems(Gender, ClothesUtils);
            return this.ClassController("ClothesBox", "ActiveBoxFromRight", "add");
        },
        ClothesBoxCloseFromClient() {
            this.ClassController("ClothesBox", "ActiveBoxFromRight", "remove");
            alt.emit(this.eventNames.WEBclient.CloseClothes);
        },
        ClothesBoxSexChangedFromClient(Sex, ClothesUtils) {
            this.AddClothesItems(Sex, ClothesUtils);
        },
        AddClothesItems(Gender, ClothesUtils) {
            if (Gender == "male") {
                this.Gender = "Male";
            } else {
                this.Gender = "Female";
            }
            this.ClothesUtils = ClothesUtils;
        },
        ChangeItemValue(Front, elemID, elem) {
            const ClothesItemValueID = document.getElementById(
                "ClothesItemValueID" + elemID
            );
            const RightBTNClothesID = document.getElementById(
                "RightBTNClothesID" + elem
            );
            const LeftBTNClothesID = document.getElementById(
                "LeftBTNClothesID" + elem
            );
            const ClothesMaximumItemValueID = document.getElementById(
                "ClothesMaximumItemValueID" + elemID
            );
            this.ResetElem(elemID);
            if (
                parseInt(ClothesItemValueID.value) >
                parseInt(ClothesMaximumItemValueID.innerHTML) ||
                parseInt(ClothesItemValueID.value) <= 0
            ) {
                ClothesItemValueID.classList.add("ClothesItemValueIsInvalid");
                ClothesItemValueID.focus();
                return;
            }
            if (Front) {
                const NumberValue = parseInt(ClothesItemValueID.value) + 1;
                if (NumberValue > parseInt(ClothesMaximumItemValueID.innerHTML)) {
                    setTimeout(() => {
                        RightBTNClothesID.classList.remove("ClothesBox_RBTNIsInvalid");
                    }, 1500);
                    return RightBTNClothesID.classList.add("ClothesBox_RBTNIsInvalid");
                }
                this.ChangeValueClothesItem(elemID, NumberValue);
                return;
            }
            const NumberValue = parseInt(ClothesItemValueID.value) - 1;
            if (NumberValue <= 0) {
                setTimeout(() => {
                    LeftBTNClothesID.classList.remove("ClothesBox_RBTNIsInvalid");
                }, 1500);
                return LeftBTNClothesID.classList.add("ClothesBox_RBTNIsInvalid");
            }
            this.ChangeValueClothesItem(elemID, NumberValue);
            return;
        },
        CheckValueForChange(elemID) {
            const ClothesItemValueID = document.getElementById('ClothesItemValueID' + elemID)
            if (ClothesItemValueID.classList.contains("ClothesItemValueIsInvalid")) {
                ClothesItemValueID.classList.remove("ClothesItemValueIsInvalid");
                ClothesItemValueID.value = 1;
                document.getElementById("ClothesShowItemValueID" + elemID).innerHTML =
                    ClothesItemValueID.value;
            }
        },
        ResetElem(ElemID) {
            const ClothesItemValueID = document.getElementById('ClothesItemValueID' + ElemID)
            ClothesItemValueID.classList.remove("ClothesItemValueIsInvalid");
        },
        ChangeClothesItemValue(elemID) {
            const ClothesItemValueID = document.getElementById('ClothesItemValueID' + elemID)
            ClothesItemValueID.blur();
            const ClothesShowItemValueID = document.getElementById(
                "ClothesShowItemValueID" + elemID
            );
            const ClothesMaximumItemValueID = document.getElementById(
                "ClothesMaximumItemValueID" + elemID
            );
            if (ClothesItemValueID.value == "") ClothesItemValueID.value = ClothesShowItemValueID.innerHTML;
            ClothesItemValueID.value = parseInt(ClothesItemValueID.value);
            if (
                ClothesItemValueID.value > parseInt(ClothesMaximumItemValueID.innerHTML) ||
                ClothesItemValueID.value <= 0
            ) {
                ClothesItemValueID.classList.add("ClothesItemValueIsInvalid");
                ClothesItemValueID.focus();
                return;
            }

            this.ChangeValueClothesItem(elemID, ClothesItemValueID.value);
        },
        ChangeValueClothesItem(elemID, value) {
            const ClothesItemValueID = document.getElementById(
                "ClothesItemValueID" + elemID
            );
            const ClothesShowItemValueID = document.getElementById(
                "ClothesShowItemValueID" + elemID
            );
            ClothesItemValueID.value = value;
            ClothesShowItemValueID.innerHTML = value;

            const SuggestionBTNs = document.getElementsByClassName('ClothesBox_BTN');
            for (let i = 0; i < SuggestionBTNs.length; i++) {
                SuggestionBTNs[i].classList.remove('ClothesSexBTNActive');
            }

            // Send Values To Client Side
            if ("alt" in window) alt.emit(this.eventNames.WEBclient.ChangeClothes, this.Gender, elemID, value);
        },
        ChangeSex(Sex) {
            if (Sex == document.getElementById("SkinGender").innerHTML.toLowerCase())
                return;

            const SuggestionBTNs = document.getElementsByClassName('ClothesBox_BTN');
            for (let i = 0; i < SuggestionBTNs.length; i++) {
                SuggestionBTNs[i].classList.remove('ClothesSexBTNActive');
            }
            if ("alt" in window) alt.emit(this.eventNames.WEBclient.ChangeSex, Sex);
        },
        ClassController(elementID, className, action) {
            if (action == "add")
                return document.getElementById(elementID).classList.add(className);
            return document.getElementById(elementID).classList.remove(className);
        },
        ScrollTo(ScrollValue) {
            return document.getElementById("SetClothesBox").scrollTo({
                top: ScrollValue,
                behavior: "smooth",
            });
        },
        KeyRowPressed(UP) {
            // if (isChatOpened) return;
            const ClothesBoxItem = document.getElementsByClassName("ClothesBoxItem");
            for (let i = 0; i < ClothesBoxItem.length; i++) {
                ClothesBoxItem[i].classList.remove("ActiveClothesItemBox");
            }
            if (UP) {
                if (this.SelectedStatus <= 0) this.SelectedStatus = ClothesBoxItem.length;
                this.SelectedStatus--;
                ClothesBoxItem[this.SelectedStatus].classList.add("ActiveClothesItemBox");
                ClothesBoxItem[this.SelectedStatus].offsetTop - 100 >= 0
                    ? this.ScrollTo(ClothesBoxItem[this.SelectedStatus].offsetTop - 100)
                    : this.ScrollTo(0);
                return;
            }
            if (this.SelectedStatus >= ClothesBoxItem.length - 1) this.SelectedStatus = -1;
            this.SelectedStatus++;
            ClothesBoxItem[this.SelectedStatus].classList.add("ActiveClothesItemBox");
            ClothesBoxItem[this.SelectedStatus].offsetTop - 100 >= 0
                ? this.ScrollTo(ClothesBoxItem[this.SelectedStatus].offsetTop - 100)
                : this.ScrollTo(0);
        },
        KeyRowLeftPressed(Left) {
            if (this.SelectedStatus <= 0) return; // For not selected item
            if (Left) {
                return document.getElementById("LeftBTNClothesID" + this.SelectedStatus).click();
            }
            return document.getElementById("RightBTNClothesID" + this.SelectedStatus).click();
        },
        SelectSuggestion(ID) {
            const SuggestionBTNs = document.getElementsByClassName('ClothesBox_BTN');
            for (let i = 0; i < SuggestionBTNs.length; i++) {
                SuggestionBTNs[i].classList.remove('ClothesSexBTNActive');
            }

            if ("alt" in window) {
                alt.emit(this.eventNames.WEBclient.Suggestion, this.Gender, ID)
            }
        },
        SetClassActiveToSuggestion(ID) {
            document.getElementById('SelectSuggestionID' + ID).classList.add('ClothesSexBTNActive');
        },
        OrderBTNClicked() {
            alt.emit(this.eventNames.WEBclient.OrderList, this.Gender);
        },
        CloseBTNClicked() {
            this.ClothesBoxCloseFromClient();
        },
    }
}
</script>

<style>
.ClothesBoxClumns_1,
.ClothesBoxClumns_2,
.ClothesBoxClumns_3,
.ClothesBoxClumns_6 {
    display: grid;
    align-items: center;
    justify-content: space-between;
    grid-template-columns: auto;
}

.ClothesBox {
    position: fixed;
    top: 50px;
    right: -500px;
    display: grid;
    grid-template-rows: auto 80px;
    width: 500px;
    height: 90%;
    opacity: 0;
    border-radius: 5px;
    overflow: hidden;
    background-color: var(--Clothes_Box_Background_Color);
    transition: 0.1s;
}

.SetClothesBox {
    background-color: var(--Clothes_Box_Background_Color);
    /* height: 50%; */
    text-align: center;
    transition: 0.5s;
    overflow-y: auto;
}

.ClothesButtonBox {
    height: 80px;
    text-align: center;
    background-color: var(--Clothes_Item_Background_Color);
    width: 100%;
    border-radius: 5px;
    z-index: 100;
    display: grid;
}

.SubClothesBox {
    width: 90%;
    display: grid;
    margin: auto;
    padding-right: 8px;
    align-items: center;
    justify-content: space-between;
    grid-template-columns: 47% 47%;
}

.SubClothesButtonBox {
    background-color: var(--Clothes_Box_Background_Color);
    border-radius: 5px;
    height: 38px;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 14px;
    font-weight: 100;
    cursor: pointer;
    color: var(--Clothes_Item_Color);
    transition: background-color 0.1s;
}

.SubClothesButtonBox:nth-child(2) {
    background-color: var(--Special_Color);
}

.SubClothesButtonBox:hover {
    background-color: var(--Clothes_Box_Background_Color_Hover);
    transition: background-color 0.1s;
}


.ActiveBoxFromRight {
    opacity: 1;
    right: 30px;
    transition: 0.5s;
}

.ClothesBoxItem {
    width: 90%;
    margin: 20px auto;
    color: var(--Clothes_Item_Title_Color);
    background-color: var(--Clothes_Item_Background_Color);
    font-size: 16px;
    font-weight: bold;
    padding: 5px 10px;
    border-radius: 5px;
    transition: transform 0.3s;
}

.ClothesBoxClumns_2 {
    grid-template-columns: auto auto;
}

.ClothesBoxClumns_3 {
    grid-template-columns: auto auto auto;
}

.ClothesBoxClumns_6 {
    grid-template-columns: auto auto auto auto auto auto;
}

.ClothesBox_BTN,
.ClothesBox_RBTN {
    background-color: var(--Clothes_Box_Background_Color);
    border-radius: 5px;
    text-align: center;
    padding: 1px 20px;
    cursor: pointer;
    transition: background-color 0.3s;
}

.ClothesBox_RBTN {
    padding: 4px 25px;
    color: var(--Clothes_Item_Color);
}

.ClothesBox_BTN:hover,
.ClothesBox_RBTN:hover {
    background-color: var(--Clothes_Box_Background_Color_Hover);
    transition: background-color 0.3s;
}

.ClothesBox_RBTNIsInvalid {
    animation: shakeBTN 1.5s;
}

.ClothesBoxClumns_SexBTN {
    grid-template-columns: 47% 47%;
}

.ClothesBoxClumns_2 .ClothesSexBTN {
    background-color: var(--Clothes_Box_Background_Color);
    border-radius: 5px;
    height: 25px;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 14px;
    font-weight: 100;
    cursor: pointer;
    color: var(--Clothes_Item_Color);
    transition: background-color 0.1s;
}

.ClothesBoxClumns_2 .ClothesSexBTN:hover {
    background-color: var(--Clothes_Box_Background_Color_Hover);
    transition: background-color 0.1s;
}

.ClothesBoxClumns_2 .ClothesSexBTNActive,
.ClothesBoxClumns_6 .ClothesSexBTNActive {
    background-color: var(--Special_Color);
    color: var(--Clothes_Item_Color);
}

.ClothesBoxClumns_2 .ClothesSexBTNActive:hover,
.ClothesBoxClumns_6 .ClothesSexBTNActive:hover,
.SubClothesButtonBox:nth-child(2):hover {
    background-color: var(--Special_Color_Hover);
}

.ClothesIndexAndLengh span:nth-child(2) {
    font-weight: bold;
}

.ClothesItemValue {
    text-align: center;
    width: auto;
    outline: none;
    border: none;
    background-color: var(--Clothes_Item_Background_Color);
    color: var(--Clothes_Item_Color);
    caret-color: var(--Clothes_Item_Color);
    border-radius: 5px;
    text-align: center;
    padding: 5px 5px;
    transition: background-color 0.3s;
    font-weight: bold;
    transition: 0.3s;
}

.ClothesItemValueIsInvalid {
    caret-color: var(--Clothes_Item_Color);
    animation: shake 1.5s forwards;
    transition: 0.3s;
}

.ActiveClothesItemBox {
    transform: scale(103%);
    transition: transform 0.3s;
}
</style>