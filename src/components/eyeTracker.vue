<template>
    <div class="eyeTrackerBox" id="eyeTrackerBox">
        <i class="fa-regular fa-eye"></i>
        <div class="eyeTrackerMenuBox" id="eyeTrackerMenuBox">
            <div class="eyeTracker_button_close" id="eyeTracker_button_close"
                @click="ButtonCloseEyeTrackerMenuPressed()"></div>
            <div class="eyeTrackerObjectBox" id="eyeTrackerObjectBox">
                <div v-for="title in ObjectFoundedtitles" :key="title.title"
                    @click="ObjectClickedFromPlayer(title.title, title.action)">
                    {{ title.title }}
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'eyeTrackerVue',
    data() {
        return {
            ObjectFoundedtitles: [],
            eventNames: {
                clientWEB: {
                    Status: "ClientWEB:eyeTracker:Status",
                    MenuStatus: "ClientWEB:eyeTracker:MenuStatus",
                    close: "ClientWEB:eyeTrackerWebView:close",
                },
                WEBclient: {
                    ButtonCloseMenuPressed: "WEBclient:eyeTracker:ButtonCloseMenuPressed",
                    ObjectSelectedFromPlayer: "WEBclient:eyeTracker:ObjectSelectedFromPlayer",
                },
            }
        }
    },
    unmounted() {
        if ("alt" in window) {
            alt.off(this.eventNames.clientWEB.Status, this.eyeTrackerStatusController);
            alt.off(this.eventNames.clientWEB.MenuStatus, this.eyeTrackerMenuStatusController);
            alt.off(this.eventNames.clientWEB.close, this.ButtonCloseEyeTrackerMenuPressed);
        }
    },
    mounted() {
        if ("alt" in window) {
            alt.on(this.eventNames.clientWEB.Status, this.eyeTrackerStatusController);
            alt.on(this.eventNames.clientWEB.MenuStatus, this.eyeTrackerMenuStatusController);
            alt.on(this.eventNames.clientWEB.close, this.ButtonCloseEyeTrackerMenuPressed);
        }
    },
    methods: {
        eyeTrackerStatusController(Status, Color = "#ffffff") {
            if (Status) {
                document
                    .getElementById("eyeTrackerBox")
                    .classList.add("eyeTrackerBoxActive");
                document.getElementById("eyeTrackerBox").style.color = Color;
                return;
            } else {
                document
                    .getElementById("eyeTrackerBox")
                    .classList.remove("eyeTrackerBoxActive");
            }
        },
        eyeTrackerMenuStatusController(Status, Objects = null) {
            if (Status) {
                document
                    .getElementById("eyeTrackerMenuBox")
                    .classList.add("eyeTrackerMenuBoxActive");
                this.ObjectFoundedtitles = []
                Object.values(Objects.titles).forEach((title) => {
                    this.ObjectFoundedtitles.push(title)
                });
            } else {
                document
                    .getElementById("eyeTrackerMenuBox")
                    .classList.remove("eyeTrackerMenuBoxActive");
            }
        },
        ButtonCloseEyeTrackerMenuPressed() {
            if ("alt" in window)
                return alt.emit(this.eventNames.WEBclient.ButtonCloseMenuPressed);
        },
        ObjectClickedFromPlayer(ObjectTitle, ObjectAction) {
            if ("alt" in window)
                return alt.emit(this.eventNames.WEBclient.ObjectSelectedFromPlayer, {
                    title: ObjectTitle,
                    action: ObjectAction,
                });
        }
    }
}
</script>

<style>
.eyeTrackerBox {
    display: flex;
    justify-content: center;
    align-content: center;
    font-size: 24px;
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    align-items: center;
    opacity: 0;
    transition: opacity 0.3s;
}

.eyeTrackerBoxActive {
    opacity: 1;
    transition: opacity 0.3s;
}

.eyeTrackerBox svg {
    z-index: 2;
}

/* Menu Style */
.eyeTrackerMenuBox {
    display: flex;
    opacity: 0;
    position: absolute;
    align-items: center;
    justify-content: center;
    z-index: 1;
    transition: 0.5s 0.2s;
}

.eyeTrackerMenuBoxActive {
    opacity: 1;
    z-index: 10;
    transition: 0.5s;
}

.eyeTracker_button_close {
    position: absolute;
    width: 48px;
    height: 48px;
    background: #5f5656;
    color: #fff;
    border: 2px solid #5f5656;
    border-radius: 50%;
    margin: 100px auto;
    outline: none;
    overflow: hidden;
    transform: scale(0);
    opacity: 0;
    transition: 0.5s 0.2s;
    cursor: pointer;
}

.eyeTrackerMenuBoxActive .eyeTracker_button_close {
    opacity: 1;
    transform: scale(1);
    transition: 0.1s;
}

.eyeTrackerMenuBoxActive .eyeTracker_button_close:before {
    width: 0px !important;
}

.eyeTrackerMenuBoxActive .eyeTracker_button_close:after {
    width: 0px !important;
}

.eyeTracker_button_close:before,
.eyeTracker_button_close:after {
    content: "";
    position: absolute;
    left: 50%;
    top: 50%;
    width: 30px;
    height: 2px;
    border-left: 8px solid currentColor;
    border-right: 8px solid currentColor;
    box-sizing: unset;
}

.eyeTracker_button_close:before {
    transform: translate3d(-50%, -50%, 0) rotate(-45deg);
    transition: all 0.2s 0.17s cubic-bezier(0.25, 0.46, 0.45, 0.94);
}

.eyeTracker_button_close:after {
    transform: translate3d(-50%, -50%, 0) rotate(45deg);
    transition: all 0.2s cubic-bezier(0.25, 0.46, 0.45, 0.94);
}

.eyeTrackerObjectBox {
    position: absolute;
    top: 30px;
    background: #5f5656;
    color: #fff;
    padding: 10px 0px;
    border-radius: 5px;
    opacity: 0;
    transform: scale(0);
    transition: 0.3s;
    width: 100px;
}

.eyeTrackerMenuBoxActive .eyeTrackerObjectBox {
    opacity: 1;
    transform: scale(1);
    transition: 0.3s 0.4s;
}

.eyeTrackerObjectBox div {
    opacity: 0;
    padding: 2px 6px;
    width: 90%;
    margin: 10px auto;
    border: 1px solid #fff;
    text-align: center;
    border-radius: 5px;
    font-size: 18px;
    transform: scale(0);
    transition: 0.3s;
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
    overflow: hidden;
}

.eyeTrackerMenuBoxActive .eyeTrackerObjectBox div {
    opacity: 1;
    transform: scale(1);
    transition: 0.3s 0.6s;
}
</style>