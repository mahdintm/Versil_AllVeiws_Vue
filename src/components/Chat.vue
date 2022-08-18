<template>
    <div class="ChatBox">
        <div class="ChatItem" id="ChatItemBox"></div>
        <div class="InputChat" id="InputChatBox">
            <input type="text" autocomplete="off" spellcheck="false" id="inputChat"
                @keydown.enter="enterKeyPressedFromInputChat()" />
        </div>
    </div>
</template>

<script>
export default {
    name: 'ChatVue',
    data() {
        return {
            inputChat: document.getElementById("inputChat"),
            isTimeStamp: true,
            indexmem: 0,
            memory: [],
            TimeStampStatus: false,
            i_chat: 0,
            isChatOpened: false,
            ChatLimit: 50,
            eventNames: {
                clientWEB: {
                    TimeStamp: "ClientWEB:Chat:TimeStamp",
                    AddMessage: "ClientWEB:Chat:AddMessage",
                    InsertSlash: "ClientWEB:Chat:InsertSlash",
                    OpenChat: "ClientWEB:Chat:OpenChat",
                    CloseChat: "ClientWEB:Chat:CloseChat",
                    Scroll: "ClientWEB:Chat:Scroll",
                    KeyRowUpPressed: "ClientWEB:Chat:KeyRowUpPressed",
                    close: "ClientWEB:ChatWebView:close",
                },
                WEBclient: {
                    CloseChat: "WEBClient:Chat:CloseChat",
                    AddMessage: "WEBClient:Chat:AddMessage",
                },
            }
        }
    },
    unmounted() {
        if ("alt" in window) {
            alt.off(this.eventNames.clientWEB.Scroll, this.SetScrollChatBoxInChatLog);
            alt.off(this.eventNames.clientWEB.InsertSlash, this.InsertSlashInChatInput);
            alt.off(this.eventNames.clientWEB.AddMessage, this.addchat);
            alt.off(this.eventNames.clientWEB.OpenChat, this.OpenChat);
            alt.off(this.eventNames.clientWEB.CloseChat, this.CloseChat);
            alt.off(this.eventNames.clientWEB.TimeStamp, this.TimeStampActiver);
            alt.off(this.eventNames.clientWEB.KeyRowUpPressed, this.KeyRowPressed);
            alt.off(this.eventNames.clientWEB.close, this.CloseChat);
        }
    },
    mounted() {
        if ("alt" in window) {
            alt.on(this.eventNames.clientWEB.Scroll, this.SetScrollChatBoxInChatLog);
            alt.on(this.eventNames.clientWEB.InsertSlash, this.InsertSlashInChatInput);
            alt.on(this.eventNames.clientWEB.AddMessage, this.addchat);
            alt.on(this.eventNames.clientWEB.OpenChat, this.OpenChat);
            alt.on(this.eventNames.clientWEB.CloseChat, this.CloseChat);
            alt.on(this.eventNames.clientWEB.TimeStamp, this.TimeStampActiver);
            alt.on(this.eventNames.clientWEB.KeyRowUpPressed, this.KeyRowPressed);
            alt.on(this.eventNames.clientWEB.close, this.CloseChat);

        }

    },
    methods: {
        SetScrollChatBoxInChatLog(Where) {
            Where ? document.getElementById("ChatItemBox").scrollBy(0, -200) : document.getElementById("ChatItemBox").scrollBy(0, 200);
        },
        InsertSlashInChatInput() {
            document.getElementById("inputChat").value = "/";
        },
        colorify(text) {
            let matches = [];
            let m = null;
            let curPos = 0;
            do {
                m = /\{[A-Fa-f0-9]{3}\}|\{[A-Fa-f0-9]{6}\}/g.exec(text.substr(curPos));
                if (!m) break;
                matches.push({
                    found: m[0],
                    index: m["index"] + curPos,
                });
                curPos = curPos + m["index"] + m[0].length;
            } while (m != null);
            if (matches.length > 0) {
                text += "</span>";
                for (let i = matches.length - 1; i >= 0; --i) {
                    let color = matches[i].found.substring(1, matches[i].found.length - 1);
                    let insertHtml =
                        (i != 0 ? "</span>" : "") + '<span style="color: #' + color + '">';
                    text =
                        text.slice(0, matches[i].index) +
                        insertHtml +
                        text.slice(matches[i].index + matches[i].found.length, text.length);
                }
            }

            return text.replaceAll("\n", "<br>");
        },
        addchat(tt, text) {
            let TimeStamp = new Date(tt);
            this.i_chat++;
            let time = `${this.addziro(TimeStamp.getHours())}:${this.addziro(
                TimeStamp.getMinutes()
            )}:${this.addziro(TimeStamp.getSeconds())}`;
            if (this.TimeStampStatus) {
                document.getElementById("ChatItemBox").innerHTML += `<div class="Chat" id="ChatText_${this.i_chat}">
    <span class="TimeStampBox ActiveTimeStamp">${this.colorify(
                    `{ff0000}[${time}]`
                )}</span> <span>${this.colorify(text)}</span>
    </div>`;
            } else {
                document.getElementById("ChatItemBox").innerHTML += `<div class="Chat" id="ChatText_${this.i_chat}">
      <span class="TimeStampBox">${this.colorify(
                    `{ff0000}[${time}]`
                )}</span> <span>${this.colorify(text)}</span>
      </div>`;
            }
            if (this.i_chat >= this.ChatLimit) {
                document.getElementById(`ChatText_${this.i_chat - (this.ChatLimit - 1)}`).outerHTML =
                    "";
            }
            document.getElementById("ChatItemBox").scrollTo(0, document.getElementById("ChatItemBox").scrollHeight);
        },
        GetDataFromMemory(Up = true) {
            if (Up) {
                if (this.indexmem - 1 < 0) return;
                this.indexmem--;
                document.getElementById("inputChat").value = this.memory[this.indexmem];
            } else {
                if (this.memory[this.indexmem] == undefined) return;
                this.indexmem++;
                if (this.memory[this.indexmem] == undefined) return (document.getElementById("inputChat").value = "");
                document.getElementById("inputChat").value = this.memory[this.indexmem];
            }
        },
        memorysystem() {
            if (document.getElementById("inputChat").value != "") {
                if (this.memory.length < 20) {
                    this.memory.push(document.getElementById("inputChat").value);
                } else {
                    this.memory.shift();
                    this.memory.push(document.getElementById("inputChat").value);
                }
                this.indexmem = this.memory.length;
            }
        },
        addziro(adad) {
            if (adad < 10) {
                return `0${adad}`;
            } else {
                return adad;
            }
        },
        TimeStampActiver(type) {
            const timeDiv = document.getElementsByClassName("TimeStampBox");
            if (type) {
                this.TimeStampStatus = true;
                for (let i = 0; i < timeDiv.length; i++) {
                    timeDiv[i].classList.add("ActiveTimeStamp");
                }
            } else {
                this.TimeStampStatus = false;
                for (let i = 0; i < timeDiv.length; i++) {
                    timeDiv[i].classList.remove("ActiveTimeStamp");
                }
            }
        },
        enterKeyPressedFromInputChat() {
            if (!document.getElementById("InputChatBox").classList.contains("ActiveInput")) return;
            if (document.getElementById("inputChat").value == "") return this.CloseChat();

            alt.emit(this.eventNames.WEBclient.AddMessage, document.getElementById("inputChat").value);
            this.memorysystem();
            document.getElementById("inputChat").value = "";
        },
        OpenChat() {
            if (document.getElementById("InputChatBox").classList.contains("ActiveInput")) return;
            document.getElementById("InputChatBox").classList.add("ActiveInput");
            document.getElementById("inputChat").focus();
            document.getElementById("ChatItemBox").classList.add("ChatItemActive");
            this.isChatOpened = true;
        },
        CloseChat(isEmit = true) {
            if (!document.getElementById("InputChatBox").classList.contains("ActiveInput")) return;
            document.getElementById("inputChat").blur();
            document.getElementById("InputChatBox").classList.remove("ActiveInput");
            document.getElementById("ChatItemBox").classList.remove("ChatItemActive");
            if ("alt" in window)
                if (isEmit)
                    alt.emit(this.eventNames.WEBclient.CloseChat);
            this.isChatOpened = false;
        },
        KeyRowPressed(up) {
            if (up == true) {
                if (!document.getElementById("InputChatBox").classList.contains("ActiveInput")) return;
                this.GetDataFromMemory(true);
            } else {
                if (!document.getElementById("InputChatBox").classList.contains("ActiveInput")) return;
                this.GetDataFromMemory(false);
            }
        }
    }
}
</script>

<style>
.ChatBox {
    width: 40%;
    height: 300px;
    display: grid;
    grid-template-rows: 85% 15%;
    margin: 20px 0px 0px 40px;
    font-size: 24px;
    font-family: var(--font-family);
}

.ChatItem {
    -webkit-text-stroke: 0.5px #000000;
    color: #ffffff;
    padding: 10px 10px 0px;
    overflow-x: hidden;
    overflow-y: hidden;
    background-color: none;
    border-radius: 5px;
    transition: background-color 0.3s;
}

.ChatItemActive {
    background-color: rgba(0, 0, 0, 0.4);
    transition: background-color 0.3s;
    overflow-y: scroll;
}

.InputChat {
    opacity: 0;
    transition: 0.3s;
}

.ActiveInput {
    opacity: 1;
    transition: 0.3s;
}

.InputChat input {
    width: 100%;
    height: 100%;
    outline: none;
    border: none;
    font-size: 22px;
    padding: 0px 10px;
    border-radius: 2px;
    margin-top: 10px;
}

.TimeStampBox {
    display: none;
}

.TimeStampBox span {
    font-family: none;
}

.ActiveTimeStamp {
    display: unset;
}
</style>