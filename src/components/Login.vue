<template>
    <div :class="{'dark' : WebData.isDarkMode , 'rtl' : WebData.isFaLanguage}" id="LoginBox">
        <div class="content-body dark-layout ">
            <div class="auth-wrapper auth-basic px-2 ">
                <div class="auth-inner my-2 ">
                    <div class="hin shadow ground ">
                        <h2 class="text-center pt-4 pb-2 "
                            style=" color: #7367f0; font-family: 'Logomotion' !important; "><small><img
                                    src="../assets/img/login/vesil_purple.png" class="img-fluid w-25-2 "
                                    alt=" "></small> versil game </h2>



                        <p class="ground text-head-1">
                            {{WebData.isFaLanguage ? WebData.LaunguageData.FA.WelcomeMsg :
                            WebData.LaunguageData.EN.WelcomeMsg}}
                        </p>
                        <p class="ground text-head-2">
                            {{WebData.isFaLanguage ? WebData.LaunguageData.FA.DetailsWelcomeMsg :
                            WebData.LaunguageData.EN.DetailsWelcomeMsg}}
                        </p>


                        <div class="back ">



                            <div class="my-2 form-floating">
                                <input type="text" class="form-control" id="LoginPage_Username" placeholder="Username"
                                    @keydown.enter="ClickLoginButton">
                                <label for="LoginPage_Username" class="form-label  text-fs"
                                    :class="WebData.isFaLanguage ?'text':'text-form'"><i
                                        class="bi bi-person-fill me-1"></i> {{WebData.isFaLanguage ?
                                        WebData.LaunguageData.FA.UsernameText :
                                        WebData.LaunguageData.EN.UsernameText}}</label>
                            </div>


                            <div class="my-3 form-floating">
                                <input type="password" class="form-control" id="LoginPage_Password"
                                    placeholder="password" @keydown.enter="ClickLoginButton">
                                <label for="LoginPage_Password" class="form-label  text-fs"
                                    :class="WebData.isFaLanguage ?'text':'text-form'"><i
                                        class="bi bi-shield-lock-fill me-1 "></i>{{WebData.isFaLanguage ?
                                        WebData.LaunguageData.FA.PasswordText :
                                        WebData.LaunguageData.EN.PasswordText}}</label>
                            </div>


                            <div class="my-1">
                                <div class="form-check text-0">
                                    <div>
                                        <label class="form-check-label"
                                            :class="WebData.isFaLanguage ?'text-fs-2':'text-fs-3'"
                                            for="RememberMeInput">{{WebData.isFaLanguage ?
                                            WebData.LaunguageData.FA.RememberText :
                                            WebData.LaunguageData.EN.RememberText}}</label>
                                        <input class="form-check-input ground " type="checkbox" id="RememberMeInput">
                                    </div>
                                    <a href="" class="text-decoration-none text-1"
                                        :class="WebData.isFaLanguage ?'float-left':'float-end'">
                                        <p class="text-fs-1 text-1 ">{{WebData.isFaLanguage ?
                                        WebData.LaunguageData.FA.ForgetPassword :
                                        WebData.LaunguageData.EN.ForgetPassword}}</p>
                                    </a>
                                </div>
                            </div>



                            <div class="">
                                <button class="btn btn-primary w-100" tabindex="4" id="LoginBTN"
                                    @click="ClickLoginButton">{{WebData.isFaLanguage ? WebData.LaunguageData.FA.SignIn :
                                    WebData.LaunguageData.EN.SignIn}}</button>
                                <p class="FooterMenuTextAlignCenter pt-4 text-fs-1">{{WebData.isFaLanguage ?
                                WebData.LaunguageData.FA.isNewAccountText :
                                WebData.LaunguageData.EN.isNewAccountText}}<a href=""
                                        class="text-decoration-none text-1 ">{{WebData.isFaLanguage ?
                                        WebData.LaunguageData.FA.CreateAccount :
                                        WebData.LaunguageData.EN.CreateAccount}}</a></p>
                            </div>


                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

</template>

<script>
export default {
    name: 'LoginVue',
    data() {
        return {
            IsLoginSuccessfully: false,
            WebData: {
                isDarkMode: false,
                isFaLanguage: true,
                LaunguageData: {
                    EN: {
                        WelcomeMsg: 'Welcome to Versil! 👋',
                        DetailsWelcomeMsg: 'Please sign-in to your account and start the adventure',
                        UsernameText: 'Username',
                        PasswordText: 'Password',
                        RememberText: 'Remember me',
                        ForgetPassword: 'Forget Password?',
                        SignIn: 'Sign in',
                        isNewAccountText: 'New on our platform? ',
                        CreateAccount: 'Create an account'
                    },
                    FA: {
                        WelcomeMsg: 'به ورسیل خوش آمدید! 👋',
                        DetailsWelcomeMsg: 'لطفا وارد حساب کاربری خود شوید و ماجراجویی را شروع کنید',
                        UsernameText: 'نام کاربری',
                        PasswordText: 'رمز عبور',
                        RememberText: 'مرا به خاطر بسپار',
                        ForgetPassword: 'فراموشی رمز؟',
                        SignIn: 'ورود',
                        isNewAccountText: 'تازه واردی؟ ',
                        CreateAccount: 'حساب کاربری خودتو بساز'
                    }
                }
            },
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
    beforeUnmount() {
        if (this.IsLoginSuccessfully)
            document.getElementById('LoginBTN').disabled = false;
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
        ClickLoginButton() {
            if (document.getElementById('LoginBTN').disabled) return
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
        },
        LoginPageIsLoginSuccessfully() {
            this.IsLoginSuccessfully = true
        },
        LoginPageSetDataWebIsHTML(object) {
            try {
                console.log(object.WebLanguage)
                this.WebData.isDarkMode = object.WebDarkMode;
                object.WebLanguage == 'fa' ? this.WebData.isFaLanguage = true : this.WebData.isFaLanguage = false

                document.getElementById('LoginPage_Username').value = object.LoginData.username;
                document.getElementById('LoginPage_Password').value = object.LoginData.password;
            } catch (error) {
                document.getElementById('LoginPage_Username').value = "";
                document.getElementById('LoginPage_Password').value = "";
            }
        },

    }
}
</script>

<style>
/* @import url(../assets/css/login/owl.carousel.min.css); */
@import url("../assets/css/login/bootstrap-icons.css");

.auth-wrapper {
    display: flex;
    flex-basis: 100%;
    min-height: 100vh;
    min-height: calc(var(--vh, 1vh) * 100);
    width: 100%;
}

.FooterMenuTextAlignCenter,
.rtl .FooterMenuTextAlignCenter {
    text-align: center !important;
}

.me-1 {
    margin: 0px 0.25rem !important;
}

.auth-wrapper .auth-inner {
    width: 100%;
}

.auth-wrapper.auth-basic {
    align-items: center;
    justify-content: center;
    overflow: hidden;
}

.auth-wrapper.auth-basic .auth-inner {
    position: relative;
}

.auth-wrapper.auth-basic .auth-inner:before {
    width: 244px;
    height: 243px;
    content: ' ';
    position: absolute;
    top: -54px;
    left: -46px;
    background-image: url("data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAPQAAADzCAMAAACG9Mt0AAAAAXNSR0IArs4c6QAAAERlWElmTU0AKgAAAAgAAYdpAAQAAAABAAAAGgAAAAAAA6ABAAMAAAABAAEAAKACAAQAAAABAAAA9KADAAQAAAABAAAA8wAAAADhQHfUAAAAyVBMVEUAAAD///+AgP+AgP9mZv+AgNWAgP9tbf9gYP+AgP9xcf9mZv+AZuaAgP9dXf90dOhiYv92dv9mZu5mZv93d+53d/9paf94afCAcfFrXvJra/9mZvJzZvJzc/JoaP96b/Rqav91aupsYvV2bOt2bPVxaPZ7cfZqavZyau1waPd4aO9xafBxafh4afB1bfh4avFuZ/F2afJzZvJzZ/N0aPN0bvN3bPR0ae5yZ/R3be93bfR1au9zafBxbPVzavV0a/F0a/ZyafFwaPKZm3nTAAAAQ3RSTlMAAQIEBQYGBwgICQoKCgsLDQ0PDw8PERESExMUFBQWFxgYGhoaGxsdHSAgIiIiIyQlJygqLCwtLi8vLzAzNDU3Nzg7h9vbHgAAA9RJREFUeNrt3ftS2kAUx/Fc1gSyWsErtuJdRDQiiteolb7/QzUoTm07k4AzObuu3/MCez45yWbzT36eZ6b8erO1e1B97baadd+zocJWmg0HaXe/+uqmg2GWtkLT5Lle1m9LdhG2+1lvzuiUO1knEF81yFc1N+35m15kZOGodz1vyLx+v2Lseq/erxtZd/NuweCTtfiwaWLOD5FnsqI7+VnP3y8afnEs3Es/1+H1qvETwuq18B7e6VlwLup1ZM8kWWQBOsrmHL7GVtxvYRZYgQ4ywae61ffsqH5Lbq20bQm6ncp9P2ehJegwE/u+rl95ttSwLrVSc2ANetAU28dSa9Cp2E623bUG3d2VWmn/wBq0XCugQYMGLdVKoOJaoiuok1NdXSW1WAUfRPtRUllflaJf5ZE/O9pXVbZUPTov5c+IDqvtRwStdTgLutoxy6GnGfYb2o+1I2gd+1OiqzfLocvVE7TSDqG1mgodaqfQZbvZC9rXjqG1X45WzqFVKVpk0LLo4lGP0ZGD6KgMnTiITkrQgXYQrYNitHISrYrRsZPouBhdcxJdK0YnTqKTYrR2Eq1BgwYNGjRo0KBBgwYNGjRo0KBBgwYNGjRo0KBBgwYNGjRo0KBBgwYNGjRo0KBBgwYNGjRo0KBBgwYNGjRo0KBBgwYNGjRo0KBBgwYNGjRoh9DH59ag86ACoSYOL61B55EUQk1s3VqDzsNHhJpYe7QGncfMSHUxaliCHgcKSXVxeWQJehwdJdXF4dAS9DgkTKqLxuibFeiXODixNi7OrEC/BP+JtbE0WrYA/RrxKNfH2YUF6NegSbk+Gk87xtErN6EsWm88fzeMXpwE9EruLns/l42io4dJFLPo2/Po1w+D6IW7t9Bt2SPx3vOOMfS7eHVZtN54ulg2go56138Ct4XRunE2Ovsmjg46WeddUoUWr6WL0fCoIYgO2/2s91fstDZQjcPL0ePt5flpdXUwqW46uMrS1j95JNpQrW0dHp9UV/uT2m416/8HVGg3qzhpBjRo0KBBgwYNGjRo0KBBgwYNGjRo0KBBgwYNGjRo0KBBgwYNGjRo0KBBgwYNGjRo0KBBgwYNGjRo0KBBgwYNGjRo0KBBgwYNGjRo0KBBgwYNGjRo0KC/FDpx0pwUo2tOomvF6NhJdFyMVk6iVTE6cBIdeF9vJyvZx/I/AzuIjsrQvoNovwzt4FamSs0Ojrp80PmvoB0zh940pb7azf1yg7t0LIt978uppzbnalfucDW92ZndLPRmKweGPduYJ+zoM5/Dk+gD5NdvLhXXPp88qcUqmEH5G5JZRs6cuxwIAAAAAElFTkSuQmCC");
}

.form-check {
    display: grid !important;
    grid-template-columns: auto auto !important;
    justify-content: space-between !important;
    padding-left: unset !important;
}

.rtl .form-check .form-check-input {
    float: left !important;
    margin-left: -1.5em !important;
}

.form-check .form-check-input {
    float: unset !important;
    margin-left: 0.5rem !important;
}

.auth-wrapper.auth-basic .auth-inner:after {
    width: 272px;
    height: 272px;
    content: ' ';
    position: absolute;
    bottom: -55px;
    right: -75px;
    background-image: url("data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAARAAAAEQCAMAAABP1NsnAAAAAXNSR0IArs4c6QAAAERlWElmTU0AKgAAAAgAAYdpAAQAAAABAAAAGgAAAAAAA6ABAAMAAAABAAEAAKACAAQAAAABAAABEKADAAQAAAABAAABEAAAAAAQWxS2AAAAwFBMVEUAAAD///+AgICAgP9VVaqqVf+qqv+AgL+AgP9mZsxmZv+ZZv+AgNWAgP9tbdttbf+Sbf+AYN+AgN+AgP9xceNmZv+AZuaAZv90dOh0dP9qav+AauqAav+AgP92dv9tbf+Abe2Abf93Zu53d+6AcO94afCAcfF5a+R5a/JzZuaAZvKAc/J5bed5bfOAaPN6b/R1auqAavR6ZvV6cPV2bOuAbPV7aPZ2be2AbfZ7au17avZ3Zu53b+57a+97a/d4aO9J6CoeAAAAQHRSTlMAAQICAwMDBAQFBQUGBgcHBwgICAkKCgoLCwwMDAwNDg4ODw8QERITExQUFBUVFhcYGBkZGhobHBwdHR4eHx8gJ5uMWwAAA/FJREFUeNrt2G1XEkEYxvHZNk2xHGzdbKFl0cTwgdSkCKzu7/+t4pw6sAjtjIueE/f8r3fMO35nZnbuy5gVGcvfzJe0rnTfGI+MggGJRUZnbpPIhJKt88nU53JnFULvyISY6KAv8vPj0vr2rYwiE2Z2B9J+uNYcyyQxwWZvaeGH3G4bMjsvI/kcwTC/V+7kLoahlITzQojP3ZFgsJCh7IJQzpX0QFj4uMiY18eDMZ9bZCF9OQahnK6cm/Y7js0sh/LF3Auv1PlQd3MxbdXYIQspV44EEEAAAWTNDAYYkKdJbNMsLzYueZbaZ2iM46RVbHBaiZ9Js+nHEdli42N9XuSen5hGp1CQTuOJQDRsD99N4gMSpYWapNH6IJo83CIeILZQFesEaber79NCWRoukOpNEnW0gXQqD81w6ACxhbrYde7VuFCYeA2QRCNIsgZISyNIqz6IyhPjOjNVIFYniK3dmKU6QdLaJUimEySrDZLrBMlrgxRKU7sxCw/EMe0CAggggADySJCqxixIkKpNEh6IozELD8RxjQACCCCAAPJIkKrGLEgQXqqAAEJjxrQLCCCAAEJjRmNGY8a0CwgggABCYwYIfQgggNCYMe0CAggggNCY0ZjRmDHtAgIIIIAAQmNGHwIIIDRmTLuAAAIIIDRmNGY0Zky7gAACCCCA0JjRhwACCI0Z0y4ggAACCI0ZjRmNGdMuIIAAAgggNGb0IYAAQmPGtAsIIIAAQmNGY0ZjxrQLCCCAAAIIjRl9CCCA0Jgx7QICCCCA0JjRmNGYMe0CAggggABCY0YfAgggNGZMu4AAAgggNGY0ZjRmTLuAAAIIIIDQmNGHAAIIjRnTLiCAAAIIjRmNGY0ZIEy7gAACCCA0ZvQhgABCY8a0CwgggABCY0ZjBgiNGdMuIIAAAgiN2f/Sh+Q6PfLaIJlOkKw2SKoTJK3dmFmdILb2tBvrBIlrg5iWRo+WqQ+SaARJ1gCJAzsxThCN16p1vNurGjNjoo42j07kAHFskoY2kEbl33U0ZgoPjXW+Rl0gkarnahqtDaJKxMPDDWIiNafGenh4gExvVhXfmk7Da6L1AVGxSby2h6MxK79Zk42ea1pJbJ48sU2zDezQ8iy1z6BBwoyjMQsvXp8YQAAhgADilRfyy+wf8WqZZUfGZihvgZiB3FybC+kCUU5XLkAo50C+gbBQdUzkAIVyejIAYfFTI1solHP2HgNCnHn5AYNy4jvpoVB6fVzL91cwzLJ9Lfd7S0jhehxO5H5/yePr1W6gHonI7fJ5ORSR/n6Q2yQanq763zuXU5LJZRKiyD/W9/pjkdPZz0/yJ8fqVyry+qQZDMjJKoDfy8bRVhHhQTwAAAAASUVORK5CYII=");
    z-index: 5;
}

@media (max-width: 575.98px) {
    .auth-wrapper.auth-basic .auth-inner:after {
        display: none;
    }
}

.auth-wrapper.auth-cover .auth-inner {
    height: 100vh;
    overflow-y: auto;
    height: calc(var(--vh, 1vh) * 100);
}

.auth-wrapper.auth-cover .brand-logo {
    position: absolute;
    top: 2rem;
    left: 2rem;
    margin: 0;
    z-index: 1;
    justify-content: unset;
}

.auth-wrapper.auth-basic .auth-inner {
    max-width: 400px;
}

@media (max-height: 825px) and (max-width: 991.98px) {
    .dark-layout .auth-wrapper .auth-inner {
        background-color: #283046;
    }

    .auth-wrapper .auth-bg {
        padding-top: 3rem;
        margin: auto 0;
    }

    .auth-wrapper .auth-inner {
        background-color: #fff;
    }

    .auth-wrapper.auth-cover .auth-inner {
        padding-bottom: 1rem;
        display: flex;
        flex-direction: column;
        flex-wrap: nowrap;
    }

    .auth-wrapper.auth-cover .brand-logo {
        position: relative;
        left: 0;
        padding-left: 1.5rem;
    }
}

.hin {
    position: relative;
    height: 500px;
    margin-bottom: 20%;
    border-radius: 7px;
    padding: 0 13px;
    z-index: 10;
}


/* --------------------------------   light  ------------------------------------- */

.ground {
    background-color: #fff;
    color: #7c7c7d;
}


/* --------------------------------  end light  ------------------------------------- */


/* --------------------------------   dark  ------------------------------------- */

.dark .dark-layout {
    color: #B4B7BD;
    background-color: #161d31;
}

.dark .ground {
    background-color: #283046;
    color: #B4B7BD;
}

.dark .dark-layout input.form-control,
.dark .form-control {
    background-color: #283046;
    color: #B4B7BD;
    border-color: #404656;
}


/* --------------------------------  end  dark  ------------------------------------- */


/* --------------------------------  rtl ------------------------------------- */
.rtl p {
    direction: rtl;
    text-align: right !important;
}

.rtl .text {
    direction: rtl;
}

.rtl .text-head-1 {
    font-weight: 500;
    font-size: 20px;
    padding-left: unset !important;
    padding-right: 0.5rem !important;
}

.rtl .text-head-2 {
    font-weight: 350;
    font-size: 15px;
    width: 85%;
    padding-left: unset !important;
    padding-right: 0.5rem !important;
}

.rtl .form-floating>.form-control-plaintext~label,
.rtl .form-floating>.form-control:focus~label,
.rtl .form-floating>.form-control:not(:placeholder-shown)~label,
.rtl .form-floating>.form-select~label {
    opacity: .65;
    transform: scale(.85) translateY(-0.5rem) translateX(3.5rem) !important;
}

.rtl .text11 {
    text-align: center;
    display: flex;
    margin-top: -1.5%;
    color: #9f9e9f;
    margin-left: 83.5%;
}

.rtl .text-0 {
    display: grid;
    grid-template-columns: auto auto;
    direction: rtl;
    justify-content: space-between;
    padding-left: 0px;
}

.rtl .text-2 {
    text-align: start;
    float: left;
}

.rtl .text-end-1 {
    font-weight: 500;
    font-size: 20px;
    text-align: right !important
}

.rtl .text-end-2 {
    font-weight: 350;
    font-size: 13px;
    text-align: right !important
}

.rtl .text-head-1 {
    font-weight: 500;
    font-size: 20px;
    text-align: end;
}

.rtl .text-head-2 {
    font-size: 13px;
    text-align: end;
    width: 100%;
}


/* --------------------------------  end rtl ------------------------------------- */

.text-head-1 {
    font-weight: 500;
    font-size: 20px;
    padding-left: 0.5rem !important;
    padding-right: unset !important;
}

.text-head-2 {
    font-weight: 350;
    font-size: 15px;
    width: 85%;
    padding-left: 0.5rem !important;
    padding-right: unset !important;
}

.text-form {
    color: #9f9e9f;
    display: flex;
    align-items: center;
}

.btn-primary {
    background-color: #7367f0 !important;
    border: none !important;
}

.btn-primary:hover {
    background-color: #8a80f6 !important;
}

.text-1 {
    color: #7367f0 !important;
}

.text-1:hover {
    color: #8a80f6 !important;
}

.back {
    padding: 1px 10px;
}

.form-floating>.form-control,
.form-floating>.form-control-plaintext,
.form-floating>.form-select {
    height: calc(2.5rem + 2px);
}

.text-fs {
    font-size: 12px;
    display: flex;
    align-items: center;
}

.text-fs-1 {
    font-size: 14px;
    text-align: center;
}

.text-fs-2 {
    font-size: 13px;
}

.text-fs-3 {
    font-weight: 400;
    font-size: 14px;
}

@media (max-width: 992px) {
    .hin {
        height: 450px;
        margin-bottom: 0px;
    }
}

.w-25-2 {
    width: 45px;
}

.h21 {
    color: var(--bs-primary);
}

@media (max-width: 575.98px) {
    .auth-wrapper.auth-basic .auth-inner:before {
        display: none;
    }
}

@media screen and (max-width: 1168px) {


    .m-s--1 {
        margin-left: -10px;
    }

}
</style>