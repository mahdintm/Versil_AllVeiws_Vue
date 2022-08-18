<template>
    <div class="LoginBox">

        <input type="text" placeholder="Username" id="LoginPage_Username" @keydown.enter="LoginToServer()"><br>
        <input type="password" placeholder="Password" id="LoginPage_Password" @keydown.enter="LoginToServer()"><br>
        <button class="LoginBTN" id="LoginBTN" @click="LoginToServer()">Click To login</button>

    </div>
</template>

<script>
export default {
    name: 'LoginVue',
    data() {
        return {
            eventNames: {
                clientWEB: {
                    SetDataWeb: "ClientWEB:Login:SetDataWeb",
                    LoginSuccessfully: "ClientWEB:Login:LoginSuccessfully",
                },
                WEBclient: {
                    LoginAccount: "WEBclient:Login:LoginAccount",
                },
            }
        }
    },
    unmounted() {
        if ("alt" in window) {
            alt.off(this.eventNames.clientWEB.LoginSuccessfully, this.LoginPageIsLoginSuccessfully);
            alt.off(this.eventNames.clientWEB.SetDataWeb, this.LoginPageSetDataWebIsHTML);
        }
    },
    mounted() {
        if ("alt" in window) {
            alt.on(this.eventNames.clientWEB.LoginSuccessfully, this.LoginPageIsLoginSuccessfully);
            alt.on(this.eventNames.clientWEB.SetDataWeb, this.LoginPageSetDataWebIsHTML);
        }

        document.getElementById('LoginPage_Username').focus()
    },
    methods: {
        LoginPageIsLoginSuccessfully() {
            document.getElementById('LoginBTN').disabled = false;
        },
        LoginPageSetDataWebIsHTML(object) {
            try {
                document.getElementById('LoginPage_Username').value = object.LoginData.username;
                document.getElementById('LoginPage_Password').value = object.LoginData.password;
            } catch (error) {
                document.getElementById('LoginPage_Username').value = "";
                document.getElementById('LoginPage_Password').value = "";
            }
        },
        LoginToServer() {
            const LoginPage_Username = document.getElementById('LoginPage_Username').value;
            const LoginPage_Passowrd = document.getElementById('LoginPage_Password').value;
            if (!LoginPage_Username) return
            if (!LoginPage_Passowrd) return
            document.getElementById('LoginBTN').disabled = true;
            if ("alt" in window) {
                alt.emit(this.eventNames.WEBclient.LoginAccount, {
                    Username: LoginPage_Username,
                    Password: LoginPage_Passowrd,
                    Remember: true,
                });
            }
        }
    }
}
</script>

<style>
.LoginBox {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    text-align: center;
}

.LoginBox input {
    border: 3px solid #cccccc;
    margin-bottom: 5px;
    padding: 5px 10px;
    border-radius: 5px;
    background: #cccccccc;
}

.LoginBox .LoginBTN {
    margin-top: 5px;
    background: #cccccccc;
    padding: 10px 20px;
    border: 3px solid #cccccc;
    border-radius: 5px;
    font-size: 24px;
    cursor: pointer;
}
</style>