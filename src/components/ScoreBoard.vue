<template>
    <div class="VGScoreBoard" id="VGScoreBoard">
        <div class="TopNavBarBox">
            <div>
                <p class="fs-1" style="font-family: 'Logomotion' !important">
                    {{ ServerName }}
                </p>
            </div>
            <div class="row mb-2" style="margin: -40px 0px 0px !important;">
                <div class="col-2 col-lg-1 text-center">ID</div>
                <div class="col-6 col-lg-9 TextLeft">Name</div>
                <div class="col-2 col-lg-1 text-center">Ping</div>
                <div class="col-2 col-lg-1 text-center">Level</div>
            </div>
        </div>
        <br>
        <div class="p-4 mt-1" style="padding-left: 0 !important; padding-right: 0 !important;">
            <br />
            <div class="row shadow-1" v-for="(PlayerDetails, index) in PlayersDetails" :key="index">
                <div class="col-2 col-lg-1 m-e-- text-center">{{ PlayerDetails.ID }}</div>
                <div class="col-6 col-lg-9 m-s--">{{ PlayerDetails.Name }}</div>
                <div class="col-2 col-lg-1 text-center">{{ PlayerDetails.Ping }} ms</div>
                <div class="col-2 col-lg-1 text-center">{{ PlayerDetails.Level }}</div>
            </div>
        </div>
        <br /><br />
        <div class="bg-navbar-2 fixed-bottom pt-2">
            <ul class="list-unstyled d-flex justify-content-center text-center mt-2">
                <li class="mx-2">Players: {{ ConnectedPlayers }} / {{ PlayersLimit }} <span class="ms-2">|</span></li>
                <li class="mx-2">Uptime: {{ UpTimeServer }} <span class="ms-2">|</span></li>
                <li class="mx-2">Play time: {{ PlayerPlayTime }}</li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ScoreBoardVue',
    data() {
        return {
            ServerName: 'versil game',
            PlayersLimit: 0,
            ConnectedPlayers: 0,
            UpTimeServer: 0,
            PlayerPlayTime: '00h 01m',
            PlayersDetails: [],
            eventNames: {
                clientWEB: {
                    SetScoreBoardDetails: "ClientWEB:ScoreBoard:SetScoreBoardDetails",
                    close: "ClientWEB:scoreBoardWebView:close",
                },
                WEBclient: {
                    CloseScoreBoard: "WEBclient:ScoreBoard:CloseScoreBoard",

                },
            }
        }
    },
    unmounted() {
        if ("alt" in window) {
            alt.off(this.eventNames.clientWEB.SetScoreBoardDetails, this.SetScoreBoardDetails)
            alt.off(this.eventNames.clientWEB.close, this.CloseScoreBoard)
        }
    },
    mounted() {
        if ("alt" in window) {
            alt.on(this.eventNames.clientWEB.SetScoreBoardDetails, this.SetScoreBoardDetails)
            alt.on(this.eventNames.clientWEB.close, this.CloseScoreBoard)
        }
    },
    methods: {
        SetScoreBoardDetails(ScoreBoardDetails) {
            this.PlayersLimit = ScoreBoardDetails.PlayersLimit;
            this.ConnectedPlayers = ScoreBoardDetails.ConnectedPlayers;
            this.UpTimeServer = ScoreBoardDetails.UpTimeServer;
            this.PlayerPlayTime = ScoreBoardDetails.PlayerPlayTime;
            this.PlayersDetails = []
            ScoreBoardDetails.PlayersDetails.forEach(PlayerDetails => {
                for (let i = 0; i < 50; i++) {
                    this.PlayersDetails.push({
                        ID: PlayerDetails.ID,
                        Name: PlayerDetails.Name,
                        Ping: PlayerDetails.Ping,
                        Level: PlayerDetails.Level
                    })
                }
            });

            document.getElementById('VGScoreBoard').classList.add('VGScoreBoardActive')
        },
        CloseScoreBoard() {
            document.getElementById('VGScoreBoard').classList.remove('VGScoreBoardActive')
            if ("alt" in window) {
                setTimeout(() => {
                    this.PlayersDetails = []
                    alt.emit(this.eventNames.WEBclient.CloseScoreBoard)
                }, 200);
            }
        }
    }
}
</script>

<style>
.VGScoreBoard {
    width: 80%;
    overflow-x: hidden;
    overflow-y: auto;
    position: fixed !important;
    height: 90%;
    background-color: #4b4b4b;
    color: #fff;
    border-radius: 5px;
    opacity: 0%;
    font-weight: 600;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    transition: 0.2s opacity;
}

.VGScoreBoardActive {
    opacity: 92%;
    transition: 0.3s opacity;
}

.TextLeft {
    text-align: left !important;
}


.TopNavBarBox {
    background-color: #333333;
    position: fixed;
    text-align: center;
    width: 100%;
    border-radius: 5px;
    padding: 10px 0 !important;
}

.bg-navbar-2 {
    background-color: #414141;
    text-align: center;
    width: 100%;
    border-radius: 5px;
}

.m-s-- {
    text-align: left !important;
}

.m-s--1 {
    margin-left: -0px;
}

.shadow-1 {
    box-shadow: none;
    padding: 10px 0px !important;
    width: 100% !important;
    margin-left: 0 !important;
}

.shadow-1:nth-child(even) {
    box-shadow: 5px 1px 25px rgb(52, 51, 51);
}
</style>