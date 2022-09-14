<template>
  <div id="VG_AllVue">
    <LoginVue v-if="LoginVue.isActive"></LoginVue>
    <ChatVue v-if="ChatVue.isActive"></ChatVue>
    <HUDVue v-if="HUDVue.isActive"></HUDVue>
    <VehicleVue v-if="VehicleVue.isActive"></VehicleVue>
    <eyeTrackerVue v-if="EyeTrackerVue.isActive"></eyeTrackerVue>
    <ClothesVue v-if="ClothesVue.isActive"></ClothesVue>
    <ScoreBoardVue v-if="ScoreBoardVue.isActive"></ScoreBoardVue>
    <!-- <TestVue v-if="false"></TestVue> -->
  </div>
</template>

<script>
import LoginVue from './components/Login.vue'
import ChatVue from './components/Chat.vue'
import HUDVue from './components/HUD.vue'
import VehicleVue from './components/Vehicle.vue'
import eyeTrackerVue from './components/eyeTracker.vue'
import ClothesVue from './components/Clothes.vue'
import ScoreBoardVue from './components/ScoreBoard.vue'
// import TestVue from './components/TestVue.vue'
export default {
  name: 'App',
  components: {
    LoginVue,
    ChatVue,
    HUDVue,
    VehicleVue,
    eyeTrackerVue,
    ClothesVue,
    ScoreBoardVue,
    // TestVue
  },
  data() {
    return {
      LoginVue: { isActive: true },
      ChatVue: { isActive: false },
      HUDVue: { isActive: false },
      VehicleVue: { isActive: false },
      EyeTrackerVue: { isActive: false },
      ClothesVue: { isActive: false },
      ScoreBoardVue: { isActive: false },
      WebViewEvents: {
        allVue: {
          mountedAndReady: "WEBclient:allVue:mountedAndReady",
        },
        login: {
          load: "ClientWEB:LoginWebView:Load",
          unLoad: "ClientWEB:LoginWebView:unLoad",
          close: "ClientWEB:LoginWebView:close",
        },
        chat: {
          load: "ClientWEB:ChatWebView:Load",
          unLoad: "ClientWEB:ChatWebView:unLoad",
          close: "ClientWEB:ChatWebView:close",
        },
        speedOmeter: {
          load: "ClientWEB:SpeedOmeterWebView:Load",
          unLoad: "ClientWEB:SpeedOmeterWebView:unLoad",
          close: "ClientWEB:SpeedOmeterWebView:close",
        },
        eyeTracker: {
          load: "ClientWEB:eyeTrackerWebView:Load",
          unLoad: "ClientWEB:eyeTrackerWebView:unLoad",
          close: "ClientWEB:eyeTrackerWebView:close",
        },
        clothes: {
          load: "ClientWEB:ClothesWebView:Load",
          unLoad: "ClientWEB:ClothesWebView:unLoad",
          close: "ClientWEB:ClothesWebView:close",
        },
        scoreBoard: {
          load: "ClientWEB:scoreBoardWebView:Load",
          unLoad: "ClientWEB:scoreBoardWebView:unLoad",
          close: "ClientWEB:scoreBoardWebView:close",
        },
        HUD: {
          load: "ClientWEB:HUD:Load",
          unLoad: "ClientWEB:HUD:unLoad",
        },
      },
    }
  },
  created() {
    if ('alt' in window) {
      alt.on(this.WebViewEvents.login.load, () => {
        this.LoginVue.isActive = true;
      })
      alt.on(this.WebViewEvents.login.unLoad, () => {
        this.LoginVue.isActive = false;
      })

      alt.on(this.WebViewEvents.chat.load, () => {
        this.ChatVue.isActive = true;
      })
      alt.on(this.WebViewEvents.chat.unLoad, () => {
        this.ChatVue.isActive = false;
      })

      alt.on(this.WebViewEvents.speedOmeter.load, () => {
        this.VehicleVue.isActive = true;
      })
      alt.on(this.WebViewEvents.speedOmeter.unLoad, () => {
        this.VehicleVue.isActive = false;
      })

      alt.on(this.WebViewEvents.eyeTracker.load, () => {
        this.EyeTrackerVue.isActive = true;
      })
      alt.on(this.WebViewEvents.eyeTracker.unLoad, () => {
        this.EyeTrackerVue.isActive = false;
      })

      alt.on(this.WebViewEvents.clothes.load, () => {
        this.ClothesVue.isActive = true;
      })
      alt.on(this.WebViewEvents.clothes.unLoad, () => {
        this.ClothesVue.isActive = false;
      })

      alt.on(this.WebViewEvents.scoreBoard.load, () => {
        this.ScoreBoardVue.isActive = true;
      })
      alt.on(this.WebViewEvents.scoreBoard.unLoad, () => {
        this.ScoreBoardVue.isActive = false;
      })

      alt.on(this.WebViewEvents.HUD.load, () => {
        this.HUDVue.isActive = true;
      })
      alt.on(this.WebViewEvents.HUD.unLoad, () => {
        this.HUDVue.isActive = false;
      })
    }
  },
  methods: {
  },
  mounted() {
    if ("alt" in window) {
      alt.emit(this.WebViewEvents.allVue.mountedAndReady);
    }
  }
}
</script>

<style>
/* body {
  background-size: cover;
  background-repeat: no-repeat;
  background-attachment: fixed;
  overflow-x: hidden !important;
  overflow-y: hidden !important;
} */

:root {
  --font-family: "IRANSans";
  --scrollbar_background: #888888;
  --scrollbar_background_hover: #555555;
  --Special_Color: #f66b0e;
  --Special_Color_Hover: #d65c0b;
  --SpeedOmeter_TextGray_Color: #808080;
  --Error_Color: #ff0000;
  --Clothes_Box_Background_Color: #252525;
  --Clothes_Box_Background_Color_Hover: #161616;
  --Clothes_Item_Background_Color: #363636;
  --Clothes_Item_Title_Color: #939393;
  --Clothes_Item_Color: #e4e4e4;
  --Inventory_Item_Box_Background_Color: #525252;
  --FontDreams: "DreamscapeSans";
  --FontDemiCond: "FranklinGothicDemiCondRegular";
  --FontBook: "FranklinGothicBookRegular";
  --Reyhaneh: "Reyhaneh";
  --BKoodak: "BKoodakBold";
  --Sans_Bold: "IRAN_Sans_Bold";
  --Sans_Regular: "IRAN_Sans_Regular";
  --circle-size: 25px;
  --spacing: 8px;
  --bs-primary: #7367F0;
}

@font-face {
  font-family: "IRANSans";
  src: url("./assets/font/IRANSans.ttf");
}

@font-face {
  font-family: "DreamscapeSans";
  src: url("./assets/font/DreamscapeSans.ttf");
}

@font-face {
  font-family: "FranklinGothicDemiCondRegular";
  src: url("./assets/font/FranklinGothicBookRegular.ttf");
}

@font-face {
  font-family: "FranklinGothicBookRegular";
  src: url("./assets/font/FranklinGothicBookRegular.ttf");
}

@font-face {
  font-family: "BKoodakBold";
  src: url("./assets/font/BKoodakBold.ttf");
}

@font-face {
  font-family: "IRAN_Sans_Bold";
  src: url("./assets/font/IRAN_Sans_Bold.ttf");
}

@font-face {
  font-family: "IRAN_Sans_Regular";
  src: url("./assets/font/IRAN_Sans_Regular.ttf");
}

@font-face {
  font-family: "Reyhaneh";
  src: url("./assets/font/Reyhaneh.ttf");
}

@font-face {
  font-family: "Logomotion";
  src: url("./assets/font/Logomotion.ttf");
}

* {
  /* font-family: var(--FontDemiCond); Set this for Login FORM */
  margin: 0;
  padding: 0;
  font-family: var(--font-family);
  border: none;
  outline: none;
  box-sizing: border-box;
  -webkit-touch-callout: none;
  -webkit-user-select: none;
  -khtml-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

body {
  background: none !important;
  overflow: hidden;
}

::-webkit-scrollbar {
  width: 5px;
  border-radius: 10px;
}

::-webkit-scrollbar-track {
  background: var(--scrollbar_background);
  border-radius: 10px;
}

::-webkit-scrollbar-thumb {
  background-color: var(--Special_Color);
  transition: 0.3s;
  border-radius: 10px;
}

::-webkit-scrollbar-thumb:hover {
  background: var(--Special_Color);
}

/* Chrome, Safari, Edge, Opera */
input[type="number"]::-webkit-outer-spin-button,
input[type="number"]::-webkit-inner-spin-button {
  -webkit-appearance: none;
  margin: 0;
}

/* Firefox */
input[type="number"] {
  -moz-appearance: textfield;
}

@keyframes shake {
  0% {
    background-color: var(--Error_Color);
    transform: translate(3px, 0);
  }

  5% {
    transform: translate(-3px, 0);
  }

  10% {
    transform: translate(1px, 0);
  }

  15% {
    transform: translate(-1px, 0);
  }

  20% {
    transform: translate(0px, 0);
  }

  80% {
    background-color: var(--Error_Color);
    color: var(--Clothes_Item_Color);
  }

  100% {
    background-color: var(--Clothes_Item_Background_Color);
    color: var(--Error_Color);
  }
}

@keyframes shakeBTN {
  0% {
    background-color: var(--Error_Color);
    transform: translate(3px, 0);
  }

  5% {
    transform: translate(-3px, 0);
  }

  10% {
    transform: translate(1px, 0);
  }

  15% {
    transform: translate(-1px, 0);
  }

  20% {
    transform: translate(0px, 0);
  }

  80% {
    background-color: var(--Error_Color);
  }

  100% {
    background-color: var(--Clothes_Item_Background_Color);
  }
}

@keyframes AlertFuelInSpeedOmeter {
  0% {
    background: linear-gradient(180.69deg,
        var(--Special_Color) 91.89%,
        var(--Special_Color) 6.08%);
  }

  50% {
    background: linear-gradient(180.69deg,
        var(--Error_Color) 91.89%,
        var(--Error_Color) 6.08%);
  }

  100% {
    background: linear-gradient(180.69deg,
        var(--Special_Color) 91.89%,
        var(--Special_Color) 6.08%);
  }
}

.MarginTop10px {
  margin-top: 10px;
}
</style>
