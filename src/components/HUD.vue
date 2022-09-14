<template>
    <div class="HUDBox">
        <div class="all">
            <div class="playerhud">
                <h2 class="playerhudjob" id="playerhudjob"></h2>
                <h2 class="playerhudcash">$<span id="playerhudcash"></span></h2>
                <div class="playercashimg" id="playercashimg">
                    <img src="../assets/img/hud/img/moneycash.png" alt="">
                </div>

                <div class="jobhud">
                    <img src="../assets/img/hud/img/moneyandjob.png" alt="">
                </div>
            </div>


            <img id="micons" class="allhudmicon" src="../assets/img/hud/Radial-Mode/mic-on.png" alt="">
            <img id="miconstext" class="allhudmicontext" src="../assets/img/hud/Radial-Mode/mic-on.png" alt="">
            <img id="miconstext" class="allhudmicontextwalk" src="../assets/img/hud/Radial-Mode/mic-on.png" alt="">
            <img id="miconstext" class="allhudmiconvenicewalk" src="../assets/img/hud/Radial-Mode/mic-on.png" alt="">
            <img id="miconsradial" class="allhudmiconradial" src="../assets/img/hud/Radial-Mode/mic-on.png" alt="">
            <img id="miconsradial" class="allhudmiconvenice" src="../assets/img/hud/Radial-Mode/mic-on.png" alt="">
            <img id="miconsradialwalk" class="allhudmiconradialwalk" src="../assets/img/hud/Radial-Mode/mic-on.png"
                alt="">
            <div class="compassgenel">
                <svg class="svg">
                    <text x="0" y="-2" stroke="black" fill="white" stroke-width="1" stroke-opacity="0.8"
                        style="font-family: 'Poppins',  sans-serif; font-weight: 800!important;"
                        text-anchor="middle">N</text>
                    <text x="360" y="-2" stroke="black" fill="white" stroke-width="1" stroke-opacity="0.8"
                        style="font-family:'Poppins', sans-serif; font-weight: 800!important;"
                        text-anchor="middle">N</text>
                    <text x="315" y="-20" stroke="black" fill="white" stroke-width="0.7" stroke-opacity="0.8"
                        style="font-size:14px; font-family: 'Poppins', sans-serif; font-weight: 800!important;"
                        text-anchor="middle">NW</text>
                    <text x="-45" y="-20" stroke="black" fill="white" stroke-width="0.7" stroke-opacity="0.8"
                        style="font-size:14px; font-family: 'Poppins', sans-serif; font-weight: 800!important;"
                        text-anchor="middle">NW</text>
                    <text x="45" y="-20" stroke="black" fill="white" stroke-width="0.7" stroke-opacity="0.8"
                        style="font-size:14px; font-family: 'Poppins', sans-serif; font-weight: 800!important;"
                        text-anchor="middle">NE</text>
                    <text x="405" y="-20" stroke="black" fill="white" stroke-width="0.7" stroke-opacity="0.8"
                        style="font-size:14px; font-family: 'Poppins', sans-serif; font-weight: 800!important;"
                        text-anchor="middle">NE</text>
                    <text x="90" y="-2" stroke="black" fill="white" stroke-width="1" stroke-opacity="0.8"
                        style="font-family:'Poppins',   sans-serif; font-weight: 800!important;"
                        text-anchor="middle">E</text>
                    <text x="135" y="-20" stroke="black" fill="white" stroke-width="0.7" stroke-opacity="0.8"
                        style="font-size:14px; font-family: 'Poppins', sans-serif; font-weight: 800!important;"
                        text-anchor="middle">SE</text>
                    <text x="180" y="-2" stroke="black" fill="white" stroke-width="1" stroke-opacity="0.8"
                        style="font-family:  'Poppins', sans-serif; font-weight: 800!important;"
                        text-anchor="middle">S</text>
                    <text x="225" y="-20" stroke="black" fill="white" stroke-width="0.7" stroke-opacity="0.8"
                        style="font-size:14px; font-family: 'Poppins', sans-serif; font-weight: 800!important;"
                        text-anchor="middle">SW</text>
                    <text x="270" y="-2" stroke="black" fill="white" stroke-width="1" stroke-opacity="0.8"
                        style="font-family: 'Poppins',  sans-serif; font-weight: 800!important;"
                        text-anchor="middle">W</text>
                </svg>
                <!-- compass lines -->
                <div class="bar">
                    <svg class="svg">
                        <rect width="3" stroke="black" fill="white" stroke-width="0.6" stroke-opacity="0.8" height="14"
                            x="-90" />
                        <rect width="3" stroke="black" fill="white" stroke-width="0.6" stroke-opacity="0.8" height="5"
                            x="-45" />
                        <rect width="4.5" stroke="black" fill="white" stroke-width="0.6" stroke-opacity="0.8"
                            height="14" x="0" />
                        <rect width="3" stroke="black" fill="white" stroke-width="0.6" stroke-opacity="0.8" height="5"
                            x="45" />
                        <rect width="4.5" stroke="black" fill="white" stroke-width="0.6" stroke-opacity="0.8"
                            height="14" x="90" />
                        <rect width="3" stroke="black" fill="white" stroke-width="0.6" stroke-opacity="0.8" height="5"
                            x="135" />
                        <rect width="4.5" stroke="black" fill="white" stroke-width="0.6" stroke-opacity="0.8"
                            height="14" x="180" />
                        <rect width="3" stroke="black" fill="white" stroke-width="0.6" stroke-opacity="0.8" height="5"
                            x="225" />
                        <rect width="4.5" stroke="black" fill="white" stroke-width="0.6" stroke-opacity="0.8"
                            height="14" x="270" />
                        <rect width="3" stroke="black" fill="white" stroke-width="0.6" stroke-opacity="0.8" height="5"
                            x="315" />
                        <rect width="4.5" stroke="black" fill="white" stroke-width="0.6" stroke-opacity="0.8"
                            height="14" x="360" />
                        <rect width="3" stroke="black" fill="white" stroke-width="0.6" stroke-opacity="0.8" height="5"
                            x="405" />
                        <rect width="3" stroke="black" fill="white" stroke-width="0.6" stroke-opacity="0.8" height="14"
                            x="450" />
                    </svg>
                </div>
            </div>
            <!-- <div class="bg">
                <img src="../assets/img/hud/img/Overall-Export.png" alt="" />
            </div> -->
            <div class="venice-hud">
                <div class="maphud">
                    <div class="maphud-wrapper">
                        <div class="saatvenice"></div>
                        <div class="streetnamevenice"></div>



                        <img class="venicemaphud" src="../assets/img/hud/img/Map-HUD.png" alt="" />
                        <div class="micbar-venice">
                            <div class="micbar-1-text mic-text"></div>
                            <div class="micbar-2-text mic-text"></div>
                            <div class="micbar-3-text mic-text"></div>
                        </div>
                        <div id="IDImageInRadarHUD" class="IDImageInRadarHUD">
                            <img src="../assets/img/hud/Text-Mode/id.png" alt="" srcset="">
                        </div>
                    </div>
                </div>

                <div class="health-bar">
                    <svg xmlns="http://www.w3.org/2000/svg" version="1.1" x="0px" y="0px" viewBox="3 0 134 34">
                        <path fill-opacity="0" stroke-width="4" stroke-linecap="round" stroke="#000000"
                            d="M133.989,34.4 L133.989,4.675 L4.690,4.675" />
                        <path id="health-bar" fill-opacity="0" stroke-linecap="round" stroke-width="5" stroke="#000000"
                            d="M133.989,34.4 L133.989,4.675 L4.690,4.675" />
                        <path id="health-bar2" fill-opacity="0" stroke-linecap="round" stroke-width="5" stroke="#fff"
                            d="M133.989,34.4 L133.989,4.675 L4.690,4.675" />
                    </svg>
                </div>
                <div class="hunger-bar">
                    <svg xmlns="http://www.w3.org/2000/svg" version="1.1" x="0px" y="0px" viewBox="3 0 134 34">
                        <path fill-opacity="0" stroke-width="4" stroke-linecap="round" stroke="#000000"
                            d="M133.989,34.4 L133.989,4.675 L4.690,4.675" />
                        <path id="hunger-bar" fill-opacity="0" stroke-linecap="round" stroke-width="5" stroke="#000000"
                            d="M133.989,34.4 L133.989,4.675 L4.690,4.675" />
                        <path id="hunger-bar2" fill-opacity="0" stroke-linecap="round" stroke-width="5" stroke="#fff"
                            d="M133.989,34.4 L133.989,4.675 L4.690,4.675" />
                    </svg>
                </div>
                <div class="armor-bar">
                    <svg xmlns="http://www.w3.org/2000/svg" version="1.1" x="0px" y="0px" viewBox="3 0 134 34">
                        <path fill-opacity="0" stroke-width="4" stroke-linecap="round" stroke="#000000"
                            d="M133.989,34.4 L133.989,4.675 L4.690,4.675" />
                        <path id="armor-bar" fill-opacity="0" stroke-linecap="round" stroke-width="5" stroke="#000000"
                            d="M133.989,34.4 L133.989,4.675 L4.690,4.675" />
                        <path id="armor-bar2" fill-opacity="0" stroke-linecap="round" stroke-width="5" stroke="#fff"
                            d="M133.989,34.4 L133.989,4.675 L4.690,4.675" />
                    </svg>
                </div>
                <div class="thirsty-bar">
                    <svg xmlns="http://www.w3.org/2000/svg" version="1.1" x="0px" y="0px" viewBox="3 0 134 34">
                        <path fill-opacity="0" stroke-width="4" stroke-linecap="round" stroke="#000000"
                            d="M133.989,34.4 L133.989,4.675 L4.690,4.675" />
                        <path id="thirsty-bar" fill-opacity="0" stroke-linecap="round" stroke-width="5" stroke="#000000"
                            d="M133.989,34.4 L133.989,4.675 L4.690,4.675" />
                        <path id="thirsty-bar2" fill-opacity="0" stroke-linecap="round" stroke-width="5" stroke="#fff"
                            d="M133.989,34.4 L133.989,4.675 L4.690,4.675" />
                    </svg>
                </div>


            </div>
            <!-- <div class="venice-hud-walk">
                <div class="maphud">
                    <div class="maphud-wrapper">



                        <div class="playerId2">
                            <p class="playerId"></p>
                        </div>
                        <div class="venicestamina2">
                            <p class="venicestamina"></p>
                        </div>
                        <img class="venicehudmapwalk" src="../assets/img/hud/Venice-Mode/on-walk-hud.png" alt="" />
                        <div class="venicemodeall">
                            <img class="venicemodemiclow" src="../assets/img/hud/Venice-Mode/mic-low-onwalk.png"
                                alt="" />
                            <img class="venicemodemicmid" src="../assets/img/hud/Venice-Mode/mic-mid-onwalk.png"
                                alt="" />
                            <img class="venicemodemichig" src="../assets/img/hud/Venice-Mode/mic-long-onwalk.png"
                                alt="" />
                        </div>
                    </div>
                </div>

                <div class="health-bar-walk">
                    <svg xmlns="http://www.w3.org/2000/svg" version="1.1" x="0px" y="0px" viewBox="3 0 134 34">
                        <path fill-opacity="0" stroke-width="4" stroke-linecap="round" stroke="#000000"
                            d="M133.989,34.4 L133.989,4.675 L4.690,4.675" />
                        <path id="health-bar33" fill-opacity="0" stroke-linecap="round" stroke-width="5"
                            stroke="#000000" d="M133.989,34.4 L133.989,4.675 L4.690,4.675" />
                        <path id="health-bar44" fill-opacity="0" stroke-linecap="round" stroke-width="5" stroke="#fff"
                            d="M133.989,34.4 L133.989,4.675 L4.690,4.675" />
                    </svg>
                </div>
                <div class="hunger-bar-walk">
                    <svg xmlns="http://www.w3.org/2000/svg" version="1.1" x="0px" y="0px" viewBox="3 0 134 34">
                        <path fill-opacity="0" stroke-width="4" stroke-linecap="round" stroke="#000000"
                            d="M133.989,34.4 L133.989,4.675 L4.690,4.675" />
                        <path id="hunger-bar55" fill-opacity="0" stroke-linecap="round" stroke-width="5"
                            stroke="#000000" d="M133.989,34.4 L133.989,4.675 L4.690,4.675" />
                        <path id="hunger-bar66" fill-opacity="0" stroke-linecap="round" stroke-width="5" stroke="#fff"
                            d="M133.989,34.4 L133.989,4.675 L4.690,4.675" />
                    </svg>
                </div>
                <div class="armor-bar-walk">
                    <svg xmlns="http://www.w3.org/2000/svg" version="1.1" x="0px" y="0px" viewBox="3 0 134 34">
                        <path fill-opacity="0" stroke-width="4" stroke-linecap="round" stroke="#000000"
                            d="M133.989,34.4 L133.989,4.675 L4.690,4.675" />
                        <path id="armor-bar77" fill-opacity="0" stroke-linecap="round" stroke-width="5" stroke="#000000"
                            d="M133.989,34.4 L133.989,4.675 L4.690,4.675" />
                        <path id="armor-bar88" fill-opacity="0" stroke-linecap="round" stroke-width="5" stroke="#fff"
                            d="M133.989,34.4 L133.989,4.675 L4.690,4.675" />
                    </svg>
                </div>
                <div class="thirsty-bar-walk">
                    <svg xmlns="http://www.w3.org/2000/svg" version="1.1" x="0px" y="0px" viewBox="3 0 134 34">
                        <path fill-opacity="0" stroke-width="4" stroke-linecap="round" stroke="#000000"
                            d="M133.989,34.4 L133.989,4.675 L4.690,4.675" />
                        <path id="thirsty-bar98" fill-opacity="0" stroke-linecap="round" stroke-width="5"
                            stroke="#000000" d="M133.989,34.4 L133.989,4.675 L4.690,4.675" />
                        <path id="thirsty-bar99" fill-opacity="0" stroke-linecap="round" stroke-width="5" stroke="#fff"
                            d="M133.989,34.4 L133.989,4.675 L4.690,4.675" />
                    </svg>
                </div>


            </div> -->
            <div class="text-hud">

                <div class="text-hud-map">
                    <div class="text-hud-map-wrapper">
                        <div class="saattext"></div>
                        <div class="streetnametext"></div>
                        <img id="text-hud-map" src="../assets/img/hud/Text-Mode/Map-HUD.png" alt="" />
                        <img class="text-hud-map-walk" src="../assets/img/hud/Text-Mode/onwalk-hud.png" alt="">
                        <div class="text-hud-icons-vehicle">
                            <div class="text-hud-health2">
                                <p class="text-hud-health"></p>
                            </div>
                            <div class="text-hud-armor2">
                                <p class="text-hud-armor"></p>
                            </div>

                            <div class="micbar-text">
                                <div class="micbar-1-text mic-text"></div>
                                <div class="micbar-2-text mic-text"></div>
                                <div class="micbar-3-text mic-text"></div>
                            </div>
                            <div class="text-hud-water2">
                                <p class="text-hud-water"></p>
                            </div>

                            <div class="text-hud-hunger2">
                                <p class="text-hud-hunger"></p>
                            </div>

                        </div>
                        <div class="text-hud-icons-onfoot">
                            <div class="text-server-id2">
                                <p class="text-server-id"></p>
                            </div>
                            <div class="text-hud-health2">
                                <p class="text-hud-health"></p>
                            </div>
                            <div class="text-hud-armor2">
                                <p class="text-hud-armor"></p>
                            </div>
                            <div class="text-hud-stress2">
                                <p class="text-hud-stress"></p>
                            </div>

                            <div class="micbar-text">
                                <div class="micbar-1-text mic-text"></div>
                                <div class="micbar-2-text mic-text"></div>
                                <div class="micbar-3-text mic-text"></div>
                            </div>
                            <div class="text-hud-water2">
                                <p class="text-hud-water"></p>
                            </div>
                            <div class="text-hud-hunger2">
                                <p class="text-hud-hunger"></p>
                            </div>

                            <div class="text-hud-stamina2">
                                <p class="text-hud-stamina"></p>
                            </div>


                        </div>

                    </div>
                </div>
            </div>
            <div class="radial-hud">
                <div class="radial-hud-map">
                    <div class="radial-hud-map-wrapper">
                        <div class="saat"></div>
                        <div class="streetname"></div>

                        <div class="radial-id">
                            <!-- <img style="width: 100%; height: auto;" src="./Radial-Mode/id.png"> -->
                            <div class="radial-id-text">2</div>
                        </div>
                        <img class="radial-hud-map-walk" src="../assets/img/hud/Radial-Mode/onwalk-hud.png" alt="">
                        <img id="radial-hud-map" src="../assets/img/hud/Radial-Mode/MapHUD.png" alt="" />
                        <div class="health-progress-bar">
                            <svg viewBox="0 0 36 36" class="circular-chart">

                                <path class="radialhealth circle" stroke-dasharray="0, 100"
                                    d="M16.493,1.501 C24.782,1.501 31.502,8.214 31.502,16.494 C31.502,24.775 24.782,31.487 16.493,31.487 C8.204,31.487 1.484,24.775 1.484,16.494 C1.484,8.214 8.204,1.501 16.493,1.501 Z"
                                    marker-end="url(#dot)" />
                                <path class="circlebg"
                                    d="M16.493,1.501 C24.782,1.501 31.502,8.214 31.502,16.494 C31.502,24.775 24.782,31.487 16.493,31.487 C8.204,31.487 1.484,24.775 1.484,16.494 C1.484,8.214 8.204,1.501 16.493,1.501 Z"
                                    marker-end="url(#dot)" />
                                <text x="18" y="20.35" class="percentage"></text>
                            </svg>
                        </div>
                        <div class="health-progress-bar-walk">
                            <svg viewBox="0 0 36 36" class="circular-chart">

                                <path class="radialhealthwalk circle" stroke-dasharray="0, 100"
                                    d="M16.493,1.501 C24.782,1.501 31.502,8.214 31.502,16.494 C31.502,24.775 24.782,31.487 16.493,31.487 C8.204,31.487 1.484,24.775 1.484,16.494 C1.484,8.214 8.204,1.501 16.493,1.501 Z"
                                    marker-end="url(#dot)" />
                                <path class="circlebg"
                                    d="M16.493,1.501 C24.782,1.501 31.502,8.214 31.502,16.494 C31.502,24.775 24.782,31.487 16.493,31.487 C8.204,31.487 1.484,24.775 1.484,16.494 C1.484,8.214 8.204,1.501 16.493,1.501 Z"
                                    marker-end="url(#dot)" />
                                <text x="18" y="20.35" class="percentage"></text>
                            </svg>
                        </div>
                        <div class="armor-progress-bar">
                            <svg viewBox="0 0 36 36" class="circular-chart">

                                <path class="radialarmor circle" stroke-dasharray="0, 100"
                                    d="M16.493,1.501 C24.782,1.501 31.502,8.214 31.502,16.494 C31.502,24.775 24.782,31.487 16.493,31.487 C8.204,31.487 1.484,24.775 1.484,16.494 C1.484,8.214 8.204,1.501 16.493,1.501 Z"
                                    marker-end="url(#dot)" />
                                <path class="circlebg"
                                    d="M16.493,1.501 C24.782,1.501 31.502,8.214 31.502,16.494 C31.502,24.775 24.782,31.487 16.493,31.487 C8.204,31.487 1.484,24.775 1.484,16.494 C1.484,8.214 8.204,1.501 16.493,1.501 Z"
                                    marker-end="url(#dot)" />
                                <text x="18" y="20.35" class="percentage"></text>
                            </svg>
                        </div>
                        <div class="armor-progress-bar-walk">
                            <svg viewBox="0 0 36 36" class="circular-chart">

                                <path class="radialarmorwalk circle" stroke-dasharray="0, 100"
                                    d="M16.493,1.501 C24.782,1.501 31.502,8.214 31.502,16.494 C31.502,24.775 24.782,31.487 16.493,31.487 C8.204,31.487 1.484,24.775 1.484,16.494 C1.484,8.214 8.204,1.501 16.493,1.501 Z"
                                    marker-end="url(#dot)" />
                                <path class="circlebg"
                                    d="M16.493,1.501 C24.782,1.501 31.502,8.214 31.502,16.494 C31.502,24.775 24.782,31.487 16.493,31.487 C8.204,31.487 1.484,24.775 1.484,16.494 C1.484,8.214 8.204,1.501 16.493,1.501 Z"
                                    marker-end="url(#dot)" />
                                <text x="18" y="20.35" class="percentage"></text>
                            </svg>
                        </div>
                        <div class="stress-progress-bar-walk">
                            <svg viewBox="0 0 36 36" class="circular-chart">

                                <path class="radialstresswalk circle" stroke-dasharray="0, 100"
                                    d="M16.493,1.501 C24.782,1.501 31.502,8.214 31.502,16.494 C31.502,24.775 24.782,31.487 16.493,31.487 C8.204,31.487 1.484,24.775 1.484,16.494 C1.484,8.214 8.204,1.501 16.493,1.501 Z"
                                    marker-end="url(#dot)" />
                                <path class="circlebg"
                                    d="M16.493,1.501 C24.782,1.501 31.502,8.214 31.502,16.494 C31.502,24.775 24.782,31.487 16.493,31.487 C8.204,31.487 1.484,24.775 1.484,16.494 C1.484,8.214 8.204,1.501 16.493,1.501 Z"
                                    marker-end="url(#dot)" />
                                <text x="18" y="20.35" class="percentage"></text>
                            </svg>
                        </div>
                        <div class="mic-progress-bar">
                            <svg viewBox="0 0 36 36" class="circular-chart">

                                <path class="radialmic circle" stroke-dasharray="0, 100"
                                    d="M16.493,1.501 C24.782,1.501 31.502,8.214 31.502,16.494 C31.502,24.775 24.782,31.487 16.493,31.487 C8.204,31.487 1.484,24.775 1.484,16.494 C1.484,8.214 8.204,1.501 16.493,1.501 Z"
                                    marker-end="url(#dot)" />
                                <path class="circlebg"
                                    d="M16.493,1.501 C24.782,1.501 31.502,8.214 31.502,16.494 C31.502,24.775 24.782,31.487 16.493,31.487 C8.204,31.487 1.484,24.775 1.484,16.494 C1.484,8.214 8.204,1.501 16.493,1.501 Z"
                                    marker-end="url(#dot)" />
                                <text x="18" y="20.35" class="percentage"></text>
                            </svg>
                        </div>
                        <div class="mic-progress-bar-walk">
                            <svg viewBox="0 0 36 36" class="circular-chart">

                                <path class="radialmicwalk circle" stroke-dasharray="0, 100"
                                    d="M16.493,1.501 C24.782,1.501 31.502,8.214 31.502,16.494 C31.502,24.775 24.782,31.487 16.493,31.487 C8.204,31.487 1.484,24.775 1.484,16.494 C1.484,8.214 8.204,1.501 16.493,1.501 Z"
                                    marker-end="url(#dot)" />
                                <path class="circlebg"
                                    d="M16.493,1.501 C24.782,1.501 31.502,8.214 31.502,16.494 C31.502,24.775 24.782,31.487 16.493,31.487 C8.204,31.487 1.484,24.775 1.484,16.494 C1.484,8.214 8.204,1.501 16.493,1.501 Z"
                                    marker-end="url(#dot)" />
                                <text x="18" y="20.35" class="percentage"></text>
                            </svg>
                        </div>

                        <div class="thirsty-progress-bar">
                            <svg viewBox="0 0 36 36" class="circular-chart">

                                <path class="radialthirsty circle" stroke-dasharray="0, 100"
                                    d="M16.493,1.501 C24.782,1.501 31.502,8.214 31.502,16.494 C31.502,24.775 24.782,31.487 16.493,31.487 C8.204,31.487 1.484,24.775 1.484,16.494 C1.484,8.214 8.204,1.501 16.493,1.501 Z"
                                    marker-end="url(#dot)" />
                                <path class="circlebg"
                                    d="M16.493,1.501 C24.782,1.501 31.502,8.214 31.502,16.494 C31.502,24.775 24.782,31.487 16.493,31.487 C8.204,31.487 1.484,24.775 1.484,16.494 C1.484,8.214 8.204,1.501 16.493,1.501 Z"
                                    marker-end="url(#dot)" />
                                <text x="18" y="20.35" class="percentage"></text>
                            </svg>
                        </div>
                        <div class="thirsty-progress-bar-walk">
                            <svg viewBox="0 0 36 36" class="circular-chart">

                                <path class="radialthirstywalk circle" stroke-dasharray="0, 100"
                                    d="M16.493,1.501 C24.782,1.501 31.502,8.214 31.502,16.494 C31.502,24.775 24.782,31.487 16.493,31.487 C8.204,31.487 1.484,24.775 1.484,16.494 C1.484,8.214 8.204,1.501 16.493,1.501 Z"
                                    marker-end="url(#dot)" />
                                <path class="circlebg"
                                    d="M16.493,1.501 C24.782,1.501 31.502,8.214 31.502,16.494 C31.502,24.775 24.782,31.487 16.493,31.487 C8.204,31.487 1.484,24.775 1.484,16.494 C1.484,8.214 8.204,1.501 16.493,1.501 Z"
                                    marker-end="url(#dot)" />
                                <text x="18" y="20.35" class="percentage"></text>
                            </svg>
                        </div>

                        <div class="hunger-progress-bar">
                            <svg viewBox="0 0 36 36" class="circular-chart">

                                <path class="radialhunger circle" stroke-dasharray="0, 100"
                                    d="M16.493,1.501 C24.782,1.501 31.502,8.214 31.502,16.494 C31.502,24.775 24.782,31.487 16.493,31.487 C8.204,31.487 1.484,24.775 1.484,16.494 C1.484,8.214 8.204,1.501 16.493,1.501 Z"
                                    marker-end="url(#dot)" />
                                <path class="circlebg"
                                    d="M16.493,1.501 C24.782,1.501 31.502,8.214 31.502,16.494 C31.502,24.775 24.782,31.487 16.493,31.487 C8.204,31.487 1.484,24.775 1.484,16.494 C1.484,8.214 8.204,1.501 16.493,1.501 Z"
                                    marker-end="url(#dot)" />
                                <text x="18" y="20.35" class="percentage"></text>
                            </svg>
                        </div>
                        <div class="hunger-progress-bar-walk">
                            <svg viewBox="0 0 36 36" class="circular-chart">

                                <path class="radialhungerwalk circle" stroke-dasharray="0, 100"
                                    d="M16.493,1.501 C24.782,1.501 31.502,8.214 31.502,16.494 C31.502,24.775 24.782,31.487 16.493,31.487 C8.204,31.487 1.484,24.775 1.484,16.494 C1.484,8.214 8.204,1.501 16.493,1.501 Z"
                                    marker-end="url(#dot)" />
                                <path class="circlebg"
                                    d="M16.493,1.501 C24.782,1.501 31.502,8.214 31.502,16.494 C31.502,24.775 24.782,31.487 16.493,31.487 C8.204,31.487 1.484,24.775 1.484,16.494 C1.484,8.214 8.204,1.501 16.493,1.501 Z"
                                    marker-end="url(#dot)" />
                                <text x="18" y="20.35" class="percentage"></text>
                            </svg>
                        </div>
                        <div class="stamina-progress-bar">
                            <svg viewBox="0 0 36 36" class="circular-chart">

                                <path class="radialstamina circle" stroke-dasharray="0, 100"
                                    d="M16.493,1.501 C24.782,1.501 31.502,8.214 31.502,16.494 C31.502,24.775 24.782,31.487 16.493,31.487 C8.204,31.487 1.484,24.775 1.484,16.494 C1.484,8.214 8.204,1.501 16.493,1.501 Z"
                                    marker-end="url(#dot)" />
                                <path class="circlebg"
                                    d="M16.493,1.501 C24.782,1.501 31.502,8.214 31.502,16.494 C31.502,24.775 24.782,31.487 16.493,31.487 C8.204,31.487 1.484,24.775 1.484,16.494 C1.484,8.214 8.204,1.501 16.493,1.501 Z"
                                    marker-end="url(#dot)" />
                                <text x="18" y="20.35" class="percentage"></text>
                            </svg>
                        </div>
                    </div>
                </div>

            </div>
            <div class="carhud">
                <img src="../assets/img/hud/img/Car-Speedometer.png" alt="" />
            </div>
            <div id="text">
                <h1 id="CarHUDSpeedText">59</h1>
                <h2 id="speed-unit-text">km/h</h2>
                <div id="gearTextBox">
                    <div id="SubgearTextBox">
                        <h2 id="NowGearText">P</h2>
                        <h2 id="NextGearText"></h2>
                    </div>
                </div>
            </div>

            <!-- <div class="compass">
        <img src="./img/Compass-Top.png" alt="" />
      </div> -->
            <div class="speedsvg">
                <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="224.21px"
                    height="222.21px">
                    <path class="hizsvg" fill-rule="evenodd" stroke="white" stroke-width="11.40px"
                        stroke-linecap="round" stroke-linejoin="round" fill="none" stroke-dasharray="0, 400"
                        d="M57.625,206.164 C57.625,206.164 10.704,175.358 10.704,115.531 C10.704,55.703 56.837,13.312 120.187,12.812 C183.538,15.000 208.817,60.233 210.817,71.233 " />
                </svg>
            </div>
            <div class="fuelsvg">
                <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="73.21px"
                    height="164.21px">
                    <path class="fuelani" fill-rule="evenodd" stroke="white" stroke-width="11.40px"
                        stroke-linecap="round" stroke-linejoin="round" fill="none" stroke-dasharray="50, 400"
                        d="M10.546,148.71 C10.546,148.71 57.439,117.288 57.439,57.509 C57.439,31.998 47.69,11.70 47.69,11.70 " />
                </svg>
            </div>
            <!-- <div id="progressbar">
        <div></div>
      </div> -->
            <div class="icons">
                <img id="seatbelt-on" src="../assets/img/hud/img/seatbelt.png" alt="" />
                <img id="cruise-on" src="../assets/img/hud/img/speedometer.png" alt="" />
                <img id="longlights-on" src="../assets/img/hud/img/car-light.png" alt="" />
                <img id="lights-on" src="../assets/img/hud/img/car-lights.png" alt="" />
                <img id="brakes-on" src="../assets/img/hud/img/brake-system-warning.png" alt="" />
                <img id="left-on" src="../assets/img/hud/img/left-arrow.png" alt="" />
                <img id="right-on" src="../assets/img/hud/img/right-arrow.png" alt="" />
                <svg xmlns="http://www.w3.org/2000/svg" id="engineColor" width="21" height="21" viewBox="0 0 21 21"
                    fill="none">
                    <g id="engine-icon" opacity="0.35" clip-path="url(#clip0)">
                        <path
                            d="M17.1416 7.1405C16.818 7.1405 16.5557 7.40285 16.5557 7.72644V8.31238H15.3838V7.72644C15.3838 7.40285 15.1214 7.1405 14.7979 7.1405H13.8687L12.8684 6.14023C12.7585 6.03035 12.6095 5.96863 12.4541 5.96863H11.8682V4.79675H12.4541C12.7777 4.79675 13.04 4.53441 13.04 4.21082C13.04 3.88722 12.7777 3.62488 12.4541 3.62488H6.5166C6.19301 3.62488 5.93066 3.88722 5.93066 4.21082C5.93066 4.53441 6.19301 4.79675 6.5166 4.79675H7.10254V5.96863H6.5166C6.36117 5.96863 6.21219 6.03035 6.1023 6.14023L5.10203 7.1405H3.00098C2.67738 7.1405 2.41504 7.40285 2.41504 7.72644V10.0702H1.24316V7.72644C1.24316 7.40285 0.98082 7.1405 0.657227 7.1405C0.333633 7.1405 0.0712891 7.40285 0.0712891 7.72644V13.5858C0.0712891 13.9094 0.333633 14.1718 0.657227 14.1718C0.98082 14.1718 1.24316 13.9094 1.24316 13.5858V11.2421H2.41504V13.5858C2.41504 13.9094 2.67738 14.1718 3.00098 14.1718H5.10203L7.27418 16.3439C7.38406 16.4538 7.53305 16.5155 7.68848 16.5155H13.626C13.8479 16.5155 14.0508 16.3901 14.1501 16.1916L15.16 14.1718H16.5557V14.7577C16.5557 15.0813 16.818 15.3436 17.1416 15.3436C18.757 15.3436 20.0713 14.0294 20.0713 12.4139V10.0702C20.0713 8.45476 18.757 7.1405 17.1416 7.1405ZM4.75879 12.9999H3.58691V8.31238H4.75879V12.9999ZM8.27441 4.79675H10.6963V5.96863H8.27441V4.79675ZM14.2119 13.4475L13.2638 15.3436H7.93117L5.93066 13.3431V7.96914L6.7593 7.1405C6.99762 7.1405 12.0013 7.1405 12.2114 7.1405L13.2116 8.14078C13.3216 8.25066 13.4705 8.31238 13.626 8.31238H14.2119C14.2119 8.55195 14.2119 13.2568 14.2119 13.4475ZM16.5557 12.9999H15.3838V9.48425H16.5557V12.9999ZM18.8994 12.4139C18.8994 13.1778 18.4096 13.8295 17.7275 14.0714C17.7275 13.6599 17.7275 8.56792 17.7275 8.41281C18.4096 8.65464 18.8994 9.30628 18.8994 10.0702V12.4139Z"
                            fill="white" />
                        <path
                            d="M11.2818 10.6562H9.88614L10.634 9.16038C10.7788 8.87092 10.6614 8.51897 10.372 8.37424C10.0825 8.22952 9.73059 8.34686 9.58586 8.63628L8.41399 10.98C8.21965 11.3687 8.50254 11.828 8.93805 11.828H10.3337L9.58582 13.3238C9.4411 13.6133 9.55844 13.9652 9.84785 14.11C10.1374 14.2547 10.4893 14.1372 10.634 13.8479L11.8059 11.5042C12.0002 11.1155 11.7173 10.6562 11.2818 10.6562Z"
                            fill="white" />
                    </g>
                    <defs>
                        <clipPath id="clip0">
                            <rect width="20" height="20" fill="white" transform="translate(0.0712891 0.0701904)" />
                        </clipPath>
                    </defs>
                </svg>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'HUDVue',
    data() {
        return {
            eventNames: {
                clientWEB: {
                    SetPlayerCashDetails: "ClientWEB:HUD:SetPlayerCashDetails",
                    SetCarHUDDetails: "ClientWEB:HUD:SetCarHUDDetails",
                    SetVeniceHUDDetails: "ClientWEB:HUD:SetVeniceHUDDetails",
                },
                WEBclient: {

                },
            }
        }
    },
    methods: {
        CarHUDManager(Details = {}) {
            if (!Details.isActiveCarHud) {
                document.getElementsByClassName('carhud')[0].style.display = 'none';
                document.getElementById('text').style.display = 'none';
                document.getElementsByClassName('speedsvg')[0].style.display = 'none';
                document.getElementsByClassName('fuelsvg')[0].style.display = 'none';
                document.getElementsByClassName('icons')[0].style.display = 'none';
                return
            }
            document.getElementsByClassName('carhud')[0].style.display = 'block';
            document.getElementById('text').style.display = 'block';
            document.getElementsByClassName('speedsvg')[0].style.display = 'block';
            document.getElementsByClassName('fuelsvg')[0].style.display = 'block';
            document.getElementsByClassName('icons')[0].style.display = 'block';

            document.getElementsByClassName('fuelani')[0].style.strokeDasharray = `${(Details.Fuel * 150) / 100}, 400`;
            document.getElementsByClassName('hizsvg')[0].style.strokeDasharray = `${Details.RPM}, 400`;

            Details.Engine ? document.getElementById('engineColor').classList.add('engineColorActive') : document.getElementById('engineColor').classList.remove('engineColorActive');
            document.getElementById('CarHUDSpeedText').innerHTML = Details.Speed;
            Details.isSeatBelt ? document.getElementById('seatbelt-on').style.display = 'block' : document.getElementById('seatbelt-on').style.display = 'none';
            Details.isCruse ? document.getElementById('cruise-on').style.display = 'block' : document.getElementById('cruise-on').style.display = 'none';
            Details.isLongLights ? document.getElementById('longlights-on').style.display = 'block' : document.getElementById('longlights-on').style.display = 'none';
            Details.isLights ? document.getElementById('lights-on').style.display = 'block' : document.getElementById('lights-on').style.display = 'none';
            Details.isHandBrake ? document.getElementById('brakes-on').style.display = 'block' : document.getElementById('brakes-on').style.display = 'none';
            Details.isHighRPM ? document.getElementsByClassName('hizsvg')[0].style.stroke = 'red' : document.getElementsByClassName('hizsvg')[0].style.stroke = 'white';
            Details.isHighRPM ? document.getElementById('NowGearText').classList.add('ShakeGear') : document.getElementById('NowGearText').classList.remove('ShakeGear');
            Details.isLeftGuide ? document.getElementById('left-on').style.display = 'block' : document.getElementById('left-on').style.display = 'none';
            Details.isRightGuide ? document.getElementById('right-on').style.display = 'block' : document.getElementById('right-on').style.display = 'none';

            if (Details.isGearUP != 'NotChanged')
                this.ChangeGearValue(Details.GearValue, Details.isGearUP)
        },
        PlayerCashHUDManager(Details = {}) {
            if (!Details.isActiveCashHUD) {
                return document.getElementsByClassName('playerhud')[0].style.display = 'none';
            }
            document.getElementsByClassName('playerhud')[0].style.display = 'block';
            // Cash
            const playerhudcash = document.getElementById('playerhudcash');
            const playercashimg = document.getElementById('playercashimg');
            playercashimg.style.display = 'block';
            playerhudcash.innerHTML = Details.playerCash;
            // Job
            const playerhudjob = document.getElementById('playerhudjob');
            playerhudjob.innerHTML = Details.playerJob;
        },
        PlayerHUDRadarVeniceManager(Details = {}) {
            if (!Details.isActiveRadarVenice) {
                return document.getElementsByClassName('venice-hud')[0].style.display = 'none';
            }
            document.getElementsByClassName('venice-hud')[0].style.display = 'block';

            document.getElementsByClassName('saatvenice')[0].innerHTML = Details.ServerTime;
            document.getElementsByClassName('streetnamevenice')[0].innerHTML = Details.PlayerName;
            document.getElementById('health-bar2').style.strokeDasharray = `${Details.HealthValue}, 400`;
            document.getElementById('hunger-bar2').style.strokeDasharray = `${Details.HungerValue}, 400`;
            document.getElementById('armor-bar2').style.strokeDasharray = `${Details.ArmorValue}, 400`;
            document.getElementById('thirsty-bar2').style.strokeDasharray = `${Details.ThirstyValue}, 400`;

            Details.isMicOn ? document.getElementsByClassName('allhudmicontext')[0].style.display = 'block' : document.getElementsByClassName('allhudmicontext')[0].style.display = 'none';
        },
        ChangeGearValue(NewValue, isUP = false) {
            const NowGearText = document.getElementById('NowGearText');
            const NextGearText = document.getElementById('NextGearText');
            const SubgearTextBox = document.getElementById('SubgearTextBox');
            NextGearText.innerHTML = NewValue;
            if (isUP) {
                SubgearTextBox.classList.add('SubgearTextBoxActiveUP');
                let translateValue = -30;
                const TranslateInterval = setInterval(() => {
                    if (translateValue > 0) {
                        NowGearText.innerHTML = NewValue;
                        NextGearText.innerHTML = "";
                        SubgearTextBox.style.transform = `translateY(0px)`;
                        SubgearTextBox.classList.remove('SubgearTextBoxActiveUP');
                        return clearInterval(TranslateInterval)
                    }
                    SubgearTextBox.style.transform = `translateY(${translateValue}px)`;
                    translateValue++
                }, 6);
            } else {
                SubgearTextBox.classList.add('SubgearTextBoxActiveDown');
                let translateValue = 0;
                const TranslateInterval = setInterval(() => {
                    if (translateValue < -30) {
                        NowGearText.innerHTML = NewValue;
                        NextGearText.innerHTML = "";
                        SubgearTextBox.classList.remove('SubgearTextBoxActiveDown');
                        SubgearTextBox.style.transform = `translateY(0px)`;
                        return clearInterval(TranslateInterval)
                    }
                    SubgearTextBox.style.transform = `translateY(${translateValue}px)`;
                    translateValue--
                }, 6);
            }
        }
    },
    unmounted() {
        if ("alt" in window) {
            alt.off(this.eventNames.clientWEB.SetPlayerCashDetails, this.PlayerCashHUDManager);
            alt.off(this.eventNames.clientWEB.SetCarHUDDetails, this.CarHUDManager);
            alt.off(this.eventNames.clientWEB.SetVeniceHUDDetails, this.PlayerHUDRadarVeniceManager);
        }
    },
    mounted() {
        this.CarHUDManager({ isActiveCarHud: false })
        this.PlayerCashHUDManager({ isActiveCashHUD: false })
        this.PlayerHUDRadarVeniceManager({ isActiveRadarVenice: false })
        // document.getElementsByClassName('venice-hud')[0].style.display = 'block';
        //     document.getElementsByClassName('allhudmicontext')[0].style.display = 'block'

        if ("alt" in window) {
            alt.on(this.eventNames.clientWEB.SetPlayerCashDetails, this.PlayerCashHUDManager);
            alt.on(this.eventNames.clientWEB.SetCarHUDDetails, this.CarHUDManager);
            alt.on(this.eventNames.clientWEB.SetVeniceHUDDetails, this.PlayerHUDRadarVeniceManager);
        }
    }
} 
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Poppins:ital,wght@1,600&display=swap");

#engineColor {
    right: 195px;
    position: absolute;
    bottom: 70px;
    width: 20px;
    height: 20px;
}

#engine-icon {
    opacity: 1;
}

#engineColor path {
    fill: #000;
    transition: fill 0.2s;
}

.engineColorActive path {
    fill: #fff !important;
}

.settings {
    display: none;
    background: url('../assets/img/hud/settings-img/Overlay.png');
    background-size: contain;
    background-repeat: no-repeat;
}

.bg img {
    position: fixed;
    width: auto;
    height: auto;
    opacity: 1;
    display: none;
}

#showhud {
    display: none;
}

.maphud {
    position: absolute;
    bottom: -2vh;
    left: 0vh;
    width: 30.585vh;
    height: 28.185vh;
    color: white;
}





.radialhunger {
    z-index: 2000;
    position: absolute;
    bottom: 1vh;
    left: 1vh;
}

#radial-hud-map {
    position: absolute;
    width: 20.5rem;
    height: 19rem;
    bottom: -2rem;


}

.maphud-wrapper {
    width: 100%;
    height: 100%;
    position: relative;
}

.radial-hud {
    display: none;
}

.text-hud {
    display: none;

}

.text-hud-icons-vehicle .micbar-text {
    position: absolute;
    left: 9.4vh;
    bottom: 1.8vh;

}

.text-hud-icons-vehicle .text-hud-health2 {
    position: absolute;
    flex: 1;
    bottom: 1.6vh;
    left: -0.7vh;
    font-size: 0.8vh;
    width: 3vh;
    text-align: center;
}

.text-hud-icons-vehicle .text-hud-armor {
    position: absolute;
    flex: 1;
    bottom: 1.6vh;
    left: 4.0vh;
    font-size: 0.8vh;
    width: 3vh;
    text-align: center;
}

.text-hud-icons-vehicle .text-hud-water {
    position: absolute;
    flex: 1;
    bottom: 1.6vh;
    left: 13.1vh;
    font-size: 0.8vh;
    width: 3vh;
    text-align: center;
}

.text-hud-icons-vehicle .text-hud-hunger {
    position: absolute;
    flex: 1;
    bottom: 1.6vh;
    left: 17.8vh;
    font-size: 0.8vh;
    width: 3vh;
    text-align: center;
}


.allhudmiconradialwalk {
    position: absolute;
    left: 35.8vh;
    bottom: 2vh;
    z-index: 100;
    display: none;
}

.allhudmicontextwalk {
    position: absolute;
    width: 0.8vh;
    height: 1.4vh;
    bottom: 2.7vh;
    left: 26vh;
    z-index: 100;
    display: none;
}

#text-hud-map {
    position: absolute;
    width: 29.9vh !important;
    height: 25.9vh !important;
    bottom: -1vh;
}

.text-hud-icons-onfoot .text-hud-health2 {
    position: absolute;
    font-size: 0.8vh;
    flex: 1;
    left: 1.6vh;
    bottom: 0.5vh;
    width: 3vh;
    text-align: center;

}


.text-hud-icons-onfoot .micbar-text {
    position: absolute;
    font-size: 0.8vh;
    flex: 1;
    left: 21.9vh;
    bottom: 0.5vh;

}

.text-hud-icons-onfoot .text-hud-armor2 {
    position: absolute;
    font-size: 0.8vh;
    flex: 1;
    left: 4.99vh;
    bottom: 0.5vh;
    width: 3vh;
    text-align: center;
}

.text-hud-icons-onfoot .text-hud-stress2 {
    position: absolute;
    font-size: 0.8vh;
    flex: 1;
    left: 8.3vh;
    bottom: 0.5vh;
    width: 3vh;
    text-align: center;
}

.text-hud-icons-onfoot .text-hud-water2 {
    position: absolute;
    font-size: 0.8vh;
    flex: 1;
    left: 11.7vh;
    bottom: 0.5vh;
    width: 3vh;
    text-align: center;
}

.text-hud-icons-onfoot .text-hud-hunger2 {
    position: absolute;
    font-size: 0.8vh;
    flex: 1;
    left: 15vh;
    bottom: 0.5vh;
    width: 3vh;
    text-align: center;
}

.text-hud-icons-onfoot .text-hud-stamina {
    position: absolute;
    font-size: 0.8vh;
    flex: 1;
    left: 18.1vh;
    bottom: 0.5vh;
    width: 3vh;
    text-align: center;
}

.text-hud-icons-onfoot .text-server-id2 {
    position: absolute;
    font-size: 0.8vh;
    flex: 1;
    left: -.99vh;
    bottom: 0.5vh;
    width: 2vh;
    text-align: center;


}

#SubgearTextBox {
    display: grid;
    grid-template-columns: 100%;
}

.SubgearTextBoxActiveDown {
    transform: translateY(0px);
}

.SubgearTextBoxActiveUP {
    transform: translateY(-30px);
}

.SubgearTextBoxActiveDown #NowGearText {
    grid-area: 1;
}

.SubgearTextBoxActiveUP #NowGearText {
    grid-area: 3;
}

#NextGearText {
    grid-area: 2;
}

#SubgearTextBox h2 {
    font-family: var(--font-family) !important;
    margin: 0;
    padding: 0;
    transform: scale(0.8) !important;
    color: #fff;
}

#gearTextBox {
    overflow: hidden;
    padding-top: 5px;
    width: 30px;
    height: 30px;
    position: absolute;
    opacity: 1;
    top: 42px;
    right: -20px;
    border-radius: 3px;
    box-shadow: 0px 0px 5px #000;
}

.ShakeGear {
    animation: shakeGear 0.3s infinite;
    transform: scale(0.5) !important;
}

@keyframes shakeGear {
    0% { transform: translate(1px, 1px) rotate(0deg); }
  10% { transform: translate(-1px, -2px) rotate(-1deg); }
  20% { transform: translate(-3px, 0px) rotate(1deg); }
  30% { transform: translate(3px, 2px) rotate(0deg); }
  40% { transform: translate(1px, -1px) rotate(1deg); }
  50% { transform: translate(-1px, 2px) rotate(-1deg); }
  60% { transform: translate(-3px, 1px) rotate(0deg); }
  70% { transform: translate(3px, 1px) rotate(-1deg); }
  80% { transform: translate(-1px, -1px) rotate(1deg); }
  90% { transform: translate(1px, 2px) rotate(0deg); }
  100% { transform: translate(1px, -2px) rotate(-1deg); }
}

.text-hud-map {
    position: absolute;
    bottom: -3vh;
    left: 0.5vh;
    width: 32.3vh;
    height: 28.185vh;
    color: white;
}

.text-hud-map-wrapper {
    position: relative;
    width: 100%;
    height: 100%;
}

.text-hud-map img {
    width: 92%;
    height: 99%;
    margin-bottom: 2vh;
}

.saattext {
    position: absolute;
    bottom: 22.3vh;
    left: 19.99vh;
    z-index: 5000;
    color: white;
    font-size: 1.5vh;

}

.saatvenice {
    position: absolute;
    bottom: 23.3vh;
    left: 20.99vh;
    z-index: 5000;
    color: white;
    font-size: 1.5vh;
}

.saat {
    position: absolute;
    bottom: 20.2vh;
    left: 20.5vh;
    z-index: 5000;
    color: white;
    font-size: 1.5vh;

}

.streetname {
    position: absolute;
    bottom: 20.2vh;
    left: 6vh;
    z-index: 5000;
    color: white;
    font-size: 1.5vh;
}

.streetnametext {
    position: absolute;
    bottom: 22.2vh;
    left: 5vh;
    z-index: 5000;
    color: white;
    font-size: 1.5vh;
}

.streetnamevenice {
    position: absolute;
    bottom: 23.4vh;
    left: 6vh;
    z-index: 5000;
    color: white;
    font-size: 1.5vh;
}

.maphud img {
    width: 100%;
    height: auto;
}

.hunger-bar {
    position: absolute;
    bottom: 1.75vh;
    width: 12.5vh;
    left: 16vh;
    height: 18.51vh;
    transition: all 0.25s linear;
}

.hunger-bar-walk {
    position: absolute;
    bottom: -8.75vh;
    width: 11.5vh;
    left: 16.65vh;
    height: 18.51vh;
    transition: all 0.25s linear;
}

.health-bar {
    position: absolute;
    bottom: 2.8vh;
    width: 12.5vh;
    left: 1.8vh;
    height: 18.51vh;
    transform: rotate(180deg);
}

.health-bar-walk {
    position: absolute;
    bottom: 1.2vh;
    width: 11.5vh;
    left: 1.8vh;
    height: 18.51vh;
    transform: rotate(180deg);
}

.armor-bar {
    position: absolute;
    bottom: 2.8vh;

    width: 12.5vh;
    left: 16vh;
    height: 18.51vh;
    -webkit-transform: scaleY(-1);
    transform: scaleY(-1);
}

.armor-bar-walk {
    position: absolute;
    bottom: 1.2vh;

    width: 11.5vh;
    left: 16.4vh;
    height: 18.51vh;
    -webkit-transform: scaleY(-1);
    transform: scaleY(-1);
}

.thirsty-bar {
    position: absolute;
    bottom: 1.75vh;
    width: 12.5vh;
    left: 2vh;
    height: 18.51vh;
    -webkit-transform: scaleX(-1);
    transform: scaleX(-1);
    transition: all 0.25s linear;
}

.thirsty-bar-walk {
    position: absolute;
    bottom: -8.75vh;
    width: 11.5vh;
    left: 1.8vh;
    height: 18.51vh;
    -webkit-transform: scaleX(-1);
    transform: scaleX(-1);
    transition: all 0.25s linear;
}


.playerId2 {
    position: absolute;
    bottom: 4.8vh;
    left: 6.7vh;
    width: 3vh;
    text-align: center;

}

.venicestamina2 {
    position: absolute;
    bottom: 4.8vh;
    left: 20vh;
    width: 3vh;
    text-align: center;


}


.radial-hud-map-walk {
    position: absolute;
    bottom: -1rem;
    left: 0.35vh;
}

.text-hud-map-walk {
    position: absolute;
    width: 20rem !important;
    height: 5rem !important;
    bottom: 0rem;
    left: 0.35vh;
}

.compass {
    position: absolute;
    left: 50%;
    transform: translateX(-50%);
    top: -1.18vh;
    z-index: -1;
}

.compass img {
    z-index: -1;
    opacity: 0.5;
}

.hizsvg {
    z-index: 10;
    transition: all 0.1s linear;
}

#thirsty-bar2 {
    transition: all 0.01s linear;
}

#hunger-bar2 {
    transition: all 0.01s linear;
}

#health-bar2 {
    transition: all 0.01s linear;
}

#armor-bar2 {
    transition: all 0.01s linear;
}

.fuelani {
    animation: fuelani 3s ease-out forwards;
    z-index: 10;
    transition: all 0.01s linear;
}

.micbar {
    position: absolute;
    left: 50%;
    bottom: 2vh;
    transform: translateX(-50%);
}

.text-hud-icons-vehicle {
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 22vh;
    position: absolute;
    left: 4.9vh;
    height: 2vh;
    bottom: 1.75vh;
}


.text-hud-icons-onfoot {
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 25vh;
    position: absolute;
    left: 3.3vh;
    height: 2vh;
    bottom: 4vh;

}



.micbar-venice {
    position: absolute;
    left: 49.75% !important;
    top: 24.35vh;
    transform: translateX(-50%);
}

.mic {
    height: 2px;
    width: 1.8vh;
    margin-bottom: 0.4vh;
    background-color: white;
    border-radius: 8px;
    display: none;
}

.mic-text {
    height: 1px;
    width: 12px;
    margin-bottom: 0.2vh;

    background: url('../assets/img/hud/Text-Mode/mic.png');
    background-size: cover;
    background-repeat: no-repeat;
}

@keyframes hizsvg {
    0% {
        stroke-dasharray: 0 400;
    }
}

@keyframes fuelani {
    0% {
        stroke-dasharray: 0 400;
    }
}




.settings {
    width: 100%;
    height: 100vh;
    position: relative;
}

.map-tab {
    display: flex;
    flex-direction: column;
    align-items: center;
    position: absolute;
    left: 3vh;
    bottom: 3vh;
}

.speedometer-tab {
    position: absolute;
    right: 3vh;
    bottom: 3vh;
}

.speedometer-tab-wrapper {
    width: 100%;
    height: 100%;
    position: relative;
}

.options-meter {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    position: absolute;
    left: 50%;
    transform: translateX(-50%);
    bottom: 5vh;
}

.middle-tab {
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
}

.select-hud-text {
    width: 49.35vh;
    height: 4.7222vh;
    margin-bottom: 5.56vh;
}

.hud-options {
    display: flex;
    align-items: center;
}

#disable-cinematic {
    display: none;
}

.map-hud-radial {
    width: 30.185vh;
    height: 27.2222vh;
    opacity: 0.6;
}

.map-hud-text {
    opacity: 0.6;

    width: 30.185vh;
    height: 27.2222vh;
}

.map-hud-venice {
    width: 32.407vh;
    height: 26.9444vh;
}

.hud-2-options {
    margin-top: 1.75vh;
    display: flex;
    align-items: center;
    justify-content: space-around;
}

.options-mph {
    width: 4.53vh;
    height: 2.31vh;
    margin-bottom: 1.5vh;
}

.options-kmh {
    width: 4.53vh;
    height: 2.31vh;
}

.speedometer-img {
    width: 23.055vh;
    height: 21.75vh;
}

.map-tab-img {
    width: 30.185vh;
    height: 24.1vh;
}

.compass-top {
    position: absolute;
    left: 50%;
    top: 0;
    transform: translateX(-50%);
}

.placeholder-hover {
    transition: transform 0.25s linear;
}

.placeholder-hover:hover {
    cursor: pointer;
    transform: scale(1.05);
}

.placeholder-translate-hover {
    transition: transform 0.25s linear;
}

.placeholder-translate-hover:hover {
    cursor: pointer;
    transform: scale(1.05) translateX(-50%);
}

.compass-bottom {
    position: absolute;
    left: 50%;
    bottom: 0;
    transform: translateX(-50%);
    width: 31.81vh;
    height: 6.76vh;
}

.compass-top-img {
    width: 31.81vh;
    height: 6.76vh;
}

.compass-onmap-img {
    position: relative;
    top: 3.95vh;
    width: 28.333vh;
    height: 7.407vh;
}

.venicemodemiclow {
    position: absolute;
    width: 0.5vh !important;
    height: 4vh !important;
    bottom: 5.2vh;
    left: 14.7vh;
}

.venicemodemicmid {
    position: absolute;
    width: 0.5vh !important;
    height: 5vh !important;
    bottom: 4.8vh;
    left: 14.7vh;
}


.venicemodemichig {
    position: absolute;
    width: 0.5vh !important;
    height: 6.4vh !important;
    bottom: 4.1vh;
    left: 14.7vh;
}

.allhudmicon {
    position: absolute;
    width: 1vh;
    height: 1.8vh;
    bottom: 2.5vh !important;
    left: 14.8vh !important;
    z-index: 100;
    display: none;
}

.allhudmiconvenicewalk {
    position: absolute;
    width: 1.1vh;
    height: 1.6vh;
    bottom: 4.57vh;
    left: 14.45vh;
    z-index: 100;
    display: none;
}

.allhudmiconvenice {
    position: absolute;
    width: 1.1vh;
    height: 1.6vh;
    bottom: 2.45vh;
    left: 14.8vh;
    z-index: 100;
    display: none;
}


.health-progress-bar {
    position: absolute;
    left: 2.85rem;
    bottom: 0.15rem;
    height: 3.55vh;
    width: 3.55vh;
    display: none;
}

.health-progress-bar-walk {
    position: absolute;
    left: 5.2rem;
    bottom: 1.5vh;
    height: 3.55vh;
    width: 3.55vh;
}

.armor-progress-bar {
    position: absolute;
    left: 6.1rem;
    bottom: 0.15rem;
    height: 3.55vh;
    width: 3.55vh;
    display: none;
}

.armor-progress-bar-walk {
    position: absolute;
    left: 8.4rem;
    bottom: 1.5vh;
    height: 3.55vh;
    width: 3.55vh;
}

.stress-progress-bar-walk {
    position: absolute;
    left: 11.45rem;
    bottom: 1.5vh;
    height: 3.55vh;
    width: 3.55vh;
    display: none;
}

.mic-progress-bar {
    left: 20.15rem;
    bottom: 0.15rem;
    height: 3.55vh;
    width: 3.55vh;
    display: block;
}






.settings {
    display: none;
    background: url('../assets/img/hud/settings-img/Overlay.png');
    background-size: contain;
    background-repeat: no-repeat;
}

.bg img {
    position: fixed;
    width: auto;
    height: auto;
    opacity: 1;
    display: none;
}

#showhud {
    display: none;
}

.maphud {
    position: absolute;
    bottom: -2vh;
    left: 0vh;
    width: 30.585vh;
    height: 28.185vh;
    color: white;
}





.radialhunger {
    z-index: 2000;
    position: absolute;
    bottom: 1vh;
    left: 1vh;
}

#radial-hud-map {
    position: absolute;
    width: 20.5rem;
    height: 19rem;
    bottom: -2rem;


}

.maphud-wrapper {
    width: 100%;
    height: 100%;
    position: relative;
}

.venice-hud {
    display: none;

}

.radial-hud {
    display: none;
}

.text-hud {
    display: none;

}

.text-hud-icons-vehicle .micbar-text {
    position: absolute;
    left: 9.4vh;
    bottom: 1.8vh;

}

.text-hud-icons-vehicle .text-hud-health2 {
    position: absolute;
    flex: 1;
    bottom: 1.6vh;
    left: -0.7vh;
    font-size: 0.8vh;
    width: 3vh;
    text-align: center;
}

.text-hud-icons-vehicle .text-hud-armor {
    position: absolute;
    flex: 1;
    bottom: 1.6vh;
    left: 4.0vh;
    font-size: 0.8vh;
    width: 3vh;
    text-align: center;
}

.text-hud-icons-vehicle .text-hud-water {
    position: absolute;
    flex: 1;
    bottom: 1.6vh;
    left: 13.1vh;
    font-size: 0.8vh;
    width: 3vh;
    text-align: center;
}

.text-hud-icons-vehicle .text-hud-hunger {
    position: absolute;
    flex: 1;
    bottom: 1.6vh;
    left: 17.8vh;
    font-size: 0.8vh;
    width: 3vh;
    text-align: center;
}


.allhudmiconradialwalk {
    position: absolute;
    left: 35.8vh;
    bottom: 2vh;
    z-index: 100;
    display: none;
}

.allhudmicontextwalk {
    position: absolute;
    width: 0.8vh;
    height: 1.4vh;
    bottom: 2.7vh;
    left: 26vh;
    z-index: 100;
    display: none;
}

#text-hud-map {
    position: absolute;
    width: 29.9vh !important;
    height: 25.9vh !important;
    bottom: -1vh;
}

.text-hud-icons-onfoot .text-hud-health2 {
    position: absolute;
    font-size: 0.8vh;
    flex: 1;
    left: 1.6vh;
    bottom: 0.5vh;
    width: 3vh;
    text-align: center;

}


.text-hud-icons-onfoot .micbar-text {
    position: absolute;
    font-size: 0.8vh;
    flex: 1;
    left: 21.9vh;
    bottom: 0.5vh;

}

.text-hud-icons-onfoot .text-hud-armor2 {
    position: absolute;
    font-size: 0.8vh;
    flex: 1;
    left: 4.99vh;
    bottom: 0.5vh;
    width: 3vh;
    text-align: center;
}

.text-hud-icons-onfoot .text-hud-stress2 {
    position: absolute;
    font-size: 0.8vh;
    flex: 1;
    left: 8.3vh;
    bottom: 0.5vh;
    width: 3vh;
    text-align: center;
}

.text-hud-icons-onfoot .text-hud-water2 {
    position: absolute;
    font-size: 0.8vh;
    flex: 1;
    left: 11.7vh;
    bottom: 0.5vh;
    width: 3vh;
    text-align: center;
}

.text-hud-icons-onfoot .text-hud-hunger2 {
    position: absolute;
    font-size: 0.8vh;
    flex: 1;
    left: 15vh;
    bottom: 0.5vh;
    width: 3vh;
    text-align: center;
}

.text-hud-icons-onfoot .text-hud-stamina {
    position: absolute;
    font-size: 0.8vh;
    flex: 1;
    left: 18.1vh;
    bottom: 0.5vh;
    width: 3vh;
    text-align: center;
}

.text-hud-icons-onfoot .text-server-id2 {
    position: absolute;
    font-size: 0.8vh;
    flex: 1;
    left: -.99vh;
    bottom: 0.5vh;
    width: 2vh;
    text-align: center;


}

.text-hud-map {
    position: absolute;
    bottom: -3vh;
    left: 0.5vh;
    width: 32.3vh;
    height: 28.185vh;
    color: white;
}

.text-hud-map-wrapper {
    position: relative;
    width: 100%;
    height: 100%;
}

.text-hud-map img {
    width: 92%;
    height: 99%;
    margin-bottom: 2vh;
}

.saattext {
    position: absolute;
    bottom: 22.3vh;
    left: 19.99vh;
    z-index: 5000;
    color: white;
    font-size: 1.5vh;

}

.saatvenice {
    position: absolute;
    bottom: 23.3vh;
    left: 20.99vh;
    z-index: 5000;
    color: white;
    font-size: 1.5vh;
}

.saat {
    position: absolute;
    bottom: 20.2vh;
    left: 20.5vh;
    z-index: 5000;
    color: white;
    font-size: 1.5vh;

}

.streetname {
    position: absolute;
    bottom: 20.2vh;
    left: 6vh;
    z-index: 5000;
    color: white;
    font-size: 1.5vh;
}

.streetnametext {
    position: absolute;
    bottom: 22.2vh;
    left: 5vh;
    z-index: 5000;
    color: white;
    font-size: 1.5vh;
}

.streetnamevenice {
    position: absolute;
    bottom: 23.4vh;
    left: 6vh;
    z-index: 5000;
    color: white;
    font-size: 1.5vh;
}

.maphud img {
    width: 100%;
    height: auto;
}

.hunger-bar {
    position: absolute;
    bottom: 1.75vh;
    width: 12.5vh;
    left: 16vh;
    height: 18.51vh;
    transition: all 0.25s linear;
}

.hunger-bar-walk {
    position: absolute;
    bottom: -8.75vh;
    width: 11.5vh;
    left: 16.65vh;
    height: 18.51vh;
    transition: all 0.25s linear;
}

.health-bar {
    position: absolute;
    bottom: 2.8vh;
    width: 12.5vh;
    left: 1.8vh;
    height: 18.51vh;
    transform: rotate(180deg);
}

.health-bar-walk {
    position: absolute;
    bottom: 1.2vh;
    width: 11.5vh;
    left: 1.8vh;
    height: 18.51vh;
    transform: rotate(180deg);
}

.armor-bar {
    position: absolute;
    bottom: 2.8vh;

    width: 12.5vh;
    left: 16vh;
    height: 18.51vh;
    -webkit-transform: scaleY(-1);
    transform: scaleY(-1);
}

.armor-bar-walk {
    position: absolute;
    bottom: 1.2vh;

    width: 11.5vh;
    left: 16.4vh;
    height: 18.51vh;
    -webkit-transform: scaleY(-1);
    transform: scaleY(-1);
}

.thirsty-bar {
    position: absolute;
    bottom: 1.75vh;
    width: 12.5vh;
    left: 2vh;
    height: 18.51vh;
    -webkit-transform: scaleX(-1);
    transform: scaleX(-1);
    transition: all 0.25s linear;
}

.thirsty-bar-walk {
    position: absolute;
    bottom: -8.75vh;
    width: 11.5vh;
    left: 1.8vh;
    height: 18.51vh;
    -webkit-transform: scaleX(-1);
    transform: scaleX(-1);
    transition: all 0.25s linear;
}


.playerId2 {
    position: absolute;
    bottom: 4.8vh;
    left: 6.7vh;
    width: 3vh;
    text-align: center;

}

.venicestamina2 {
    position: absolute;
    bottom: 4.8vh;
    left: 20vh;
    width: 3vh;
    text-align: center;


}

.carhud {
    position: absolute;
    bottom: 25px;
    right: 20px;
    transform: scale(0.98);
}

#text {
    position: absolute;
    font-family: "Poppins";
    font-style: normal;
    color: white;
    z-index: 2;
    bottom: 70px;
    right: 100px;
    transform: scale(1.2);
    text-align: center;
    text-anchor: middle;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}


.radial-hud-map-walk {
    position: absolute;
    bottom: -1rem;
    left: 0.35vh;
}

.text-hud-map-walk {
    position: absolute;
    width: 20rem !important;
    height: 5rem !important;
    bottom: 0rem;
    left: 0.35vh;
}

#text h2 {
    font-family: "Poppins";
    font-style: normal;
    color: white;
    z-index: 2;
    margin-top: -7px;
    transform: scale(0.5);
}

.compass {
    position: absolute;
    left: 50%;
    transform: translateX(-50%);
    top: -1.18vh;
    z-index: -1;
}

.compass img {
    z-index: -1;
    opacity: 0.5;
}

.speedsvg {
    position: absolute;
    bottom: 34.6px;
    right: 36.2px;
    stroke: white;
    transform: rotate(1.1deg);
}

.fuelsvg {
    position: absolute;
    bottom: 35.5px;
    right: 22.5px;
    stroke: white;
    transform: rotate(-1.15deg);
}

.hizsvg {
    z-index: 10;
    transition: all 0.01s linear;
}

#thirsty-bar2 {
    transition: all 0.01s linear;
}

#hunger-bar2 {
    transition: all 0.01s linear;
}

#health-bar2 {
    transition: all 0.01s linear;
}

#armor-bar2 {
    transition: all 0.01s linear;
}

.fuelani {
    animation: fuelani 3s ease-out forwards;
    z-index: 10;
    transition: all 0.01s linear;
}

#seatbelt-on {
    position: absolute;
    bottom: 60px;
    right: 182px;
    display: none;
}

#cruise-on {
    position: absolute;
    bottom: 60.1px;
    right: 154.52px;
    display: none;
}

#longlights-on {
    position: absolute;
    bottom: 59.8px;
    right: 126px;
    display: none;
}

#lights-on {
    position: absolute;
    bottom: 60.5px;
    right: 96px;
    display: none;
}

#brakes-on {
    position: absolute;
    bottom: 152px;
    right: 101px;
    display: none;
}

#left-on {
    position: absolute;
    bottom: 133.6px;
    right: 200.6px;
    display: none;
}

#right-on {
    position: absolute;
    bottom: 134px;
    right: 79px;
    display: none;
}

.micbar {
    position: absolute;
    left: 50%;
    bottom: 2vh;
    transform: translateX(-50%);
}

.text-hud-icons-vehicle {
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 22vh;
    position: absolute;
    left: 4.9vh;
    height: 2vh;
    bottom: 1.75vh;
}


.text-hud-icons-onfoot {
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 25vh;
    position: absolute;
    left: 3.3vh;
    height: 2vh;
    bottom: 4vh;

}



.micbar-venice {
    position: absolute;
    left: 49.75% !important;
    top: 24.35vh;
    transform: translateX(-50%);
}

.mic {
    height: 2px;
    width: 1.8vh;
    margin-bottom: 0.4vh;
    background-color: white;
    border-radius: 8px;
    display: none;
}

.mic-text {
    height: 1px;
    width: 12px;
    margin-bottom: 0.2vh;

    background: url('../assets/img/hud/Text-Mode/mic.png');
    background-size: cover;
    background-repeat: no-repeat;
}

@keyframes hizsvg {
    0% {
        stroke-dasharray: 0 400;
    }
}

@keyframes fuelani {
    0% {
        stroke-dasharray: 0 400;
    }
}




.settings {
    width: 100%;
    height: 100vh;
    position: relative;
}

.map-tab {
    display: flex;
    flex-direction: column;
    align-items: center;
    position: absolute;
    left: 3vh;
    bottom: 3vh;
}

.speedometer-tab {
    position: absolute;
    right: 3vh;
    bottom: 3vh;
}

.speedometer-tab-wrapper {
    width: 100%;
    height: 100%;
    position: relative;
}

.options-meter {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    position: absolute;
    left: 50%;
    transform: translateX(-50%);
    bottom: 5vh;
}

.middle-tab {
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
}

.select-hud-text {
    width: 49.35vh;
    height: 4.7222vh;
    margin-bottom: 5.56vh;
}

.hud-options {
    display: flex;
    align-items: center;
}

#disable-cinematic {
    display: none;
}

.map-hud-radial {
    width: 30.185vh;
    height: 27.2222vh;
    opacity: 0.6;
}

.map-hud-text {
    opacity: 0.6;

    width: 30.185vh;
    height: 27.2222vh;
}

.map-hud-venice {
    width: 32.407vh;
    height: 26.9444vh;
}

.hud-2-options {
    margin-top: 1.75vh;
    display: flex;
    align-items: center;
    justify-content: space-around;
}

.options-mph {
    width: 4.53vh;
    height: 2.31vh;
    margin-bottom: 1.5vh;
}

.options-kmh {
    width: 4.53vh;
    height: 2.31vh;
}

.speedometer-img {
    width: 23.055vh;
    height: 21.75vh;
}

.map-tab-img {
    width: 30.185vh;
    height: 24.1vh;
}

.compass-top {
    position: absolute;
    left: 50%;
    top: 0;
    transform: translateX(-50%);
}

.placeholder-hover {
    transition: transform 0.25s linear;
}

.placeholder-hover:hover {
    cursor: pointer;
    transform: scale(1.05);
}

.placeholder-translate-hover {
    transition: transform 0.25s linear;
}

.placeholder-translate-hover:hover {
    cursor: pointer;
    transform: scale(1.05) translateX(-50%);
}

.compass-bottom {
    position: absolute;
    left: 50%;
    bottom: 0;
    transform: translateX(-50%);
    width: 31.81vh;
    height: 6.76vh;
}

.compass-top-img {
    width: 31.81vh;
    height: 6.76vh;
}

.compass-onmap-img {
    position: relative;
    top: 3.95vh;
    width: 28.333vh;
    height: 7.407vh;
}

.venicemodemiclow {
    position: absolute;
    width: 0.5vh !important;
    height: 4vh !important;
    bottom: 5.2vh;
    left: 14.7vh;
}

.venicemodemicmid {
    position: absolute;
    width: 0.5vh !important;
    height: 5vh !important;
    bottom: 4.8vh;
    left: 14.7vh;
}


.venicemodemichig {
    position: absolute;
    width: 0.5vh !important;
    height: 6.4vh !important;
    bottom: 4.1vh;
    left: 14.7vh;
}

.allhudmicontext {
    position: absolute;
    width: 0.9vh;
    height: 1.6vh;
    bottom: 2.9vh;
    left: 14.88vh;
    z-index: 100;
    display: none;
}

.allhudmiconvenicewalk {
    position: absolute;
    width: 1.1vh;
    height: 1.6vh;
    bottom: 4.57vh;
    left: 14.45vh;
    z-index: 100;
    display: none;
}

.allhudmiconvenice {
    position: absolute;
    width: 1.1vh;
    height: 1.6vh;
    bottom: 2.45vh;
    left: 14.8vh;
    z-index: 100;
    display: none;
}

.allhudmiconradial {
    position: absolute;
    left: 14.7vh;
    bottom: 0.7vh;
    z-index: 100;
    display: none;
}


.health-progress-bar {
    position: absolute;
    left: 2.85rem;
    bottom: 0.15rem;
    height: 3.55vh;
    width: 3.55vh;
    display: none;
}

.health-progress-bar-walk {
    position: absolute;
    left: 5.2rem;
    bottom: 1.5vh;
    height: 3.55vh;
    width: 3.55vh;
}

.armor-progress-bar {
    position: absolute;
    left: 6.1rem;
    bottom: 0.15rem;
    height: 3.55vh;
    width: 3.55vh;
    display: none;
}

.armor-progress-bar-walk {
    position: absolute;
    left: 8.4rem;
    bottom: 1.5vh;
    height: 3.55vh;
    width: 3.55vh;
}

.stress-progress-bar-walk {
    position: absolute;
    left: 11.45rem;
    bottom: 1.5vh;
    height: 3.55vh;
    width: 3.55vh;
}

.mic-progress-bar {
    position: absolute;
    left: 9.15rem;
    bottom: 0.15rem;
    height: 3.55vh;
    width: 3.55vh;
    display: block;
}


.mic-progress-bar {
    position: absolute;
    left: 9.15rem;
    bottom: 0.15rem;
    height: 3.55vh;
    width: 3.55vh;
    display: block;
}

.mic-progress-bar-walk {
    position: absolute;
    left: 23.35rem;
    bottom: 1.5vh;
    height: 3.55vh;
    width: 3.55vh;
}

.thirsty-progress-bar {
    position: absolute;
    left: 12.3rem;
    bottom: 0.15rem;
    height: 3.55vh;
    width: 3.55vh;
    display: none;
}

.thirsty-progress-bar-walk {
    position: absolute;
    left: 14.59rem;
    bottom: 1.5vh;
    height: 3.55vh;
    width: 3.55vh;
}

.hunger-progress-bar {
    position: absolute;
    left: 15.4rem;
    bottom: 0.15rem;
    height: 3.55vh;
    width: 3.55vh;
    display: none;
}


.hunger-progress-bar-walk {
    position: absolute;
    left: 17.69rem;
    bottom: 1.5vh;
    height: 3.55vh;
    width: 3.55vh;
}

.stamina-progress-bar {
    position: absolute;
    left: 20.5rem;
    bottom: 1.5vh;
    display: none;
    height: 3.55vh;
    width: 3.55vh;
}

.circular-chart {
    display: block;
    margin: 10px auto;
    max-width: 80%;
    max-height: 250px;
}

.circlebg {
    position: relative;
    z-index: -100;
    stroke: #595959;
    fill: none;
    stroke-width: 2;
    stroke-linecap: round;
    opacity: 0.1;

}

.circle {
    position: relative;
    z-index: 1;
    stroke: #ffffff;
    fill: none;
    stroke-width: 2.8;
    stroke-linecap: round;
    animation: progress 3s ease-out forwards;
}

.circle-handle {
    display: none;
    position: absolute;
    height: 29px;
    width: 29px;
    border-radius: 20px;
    background: #ffffff;
    bottom: 57px;
    left: 156px;
}

@keyframes progress {
    0% {
        stroke-dasharray: 0 100;
    }
}

.compassgenel {
    position: absolute;
    top: 2vh;
    left: 50%;
    width: 150px;
    height: 300px;
    transform: translateX(-50%);
    z-index: 1000;
    overflow: hidden;
    display: none;
}


.svg {
    transform: scale(1.2);
    display: block;
    width: 100%;
    height: 80px;
    font-size: 20pt;
}

.bar {

    position: absolute;
    top: -3.5vh;
    color: rgba(255, 255, 255, 1);
    text-shadow: #000 0px 0px 1px #000 0px 0px 1px #000 0px 0px 1px;
}

.bar2 {

    position: absolute;
    font-size: 20pt;
    left: 49%;
    font-family: 'Work Sans',
        sans-serif;
    font-weight: 800 !important;
    color: white;
    text-shadow: 0px 0px 0 #000, 0px 0px 0 #000, 0px 1px 0 #000, 0px 0px 0 #000, 0px 0px 0 #000, 0px 0px 0 #000, -1px 0px 0 #000, 0px -1px 0 #000;
    top: -0.5vh;
    color: rgba(255, 255, 255, 1);
    text-shadow: #000 0px 0px 1px #000 0px 0px 1px #000 0px 0px 1px;
}




.radial-id-text {
    position: relative;
    bottom: 0.5vh;
    left: -0.1vh;

    color: white;
    font-size: 0.83vh;
}


.radial-id {
    display: flex;
    flex-direction: column;
    position: absolute;
    left: 4.7vh;
    bottom: 0.5vh;
    height: 1.35vh;
    justify-content: center;
    align-items: center;
    width: 1.35vh;
    z-index: 59999;
    text-align: center;
}












.venicehudmapwalk {
    position: absolute;
    width: 30vh !important;
    height: 12vh !important;
    bottom: 1vh;

}

#progressbar {
    position: absolute;
    border-radius: 13px;
    width: 90px;
    right: 129px;
    bottom: 35px;
    height: 9px;
}

#progressbar>div {
    background-color: white;
    width: 100%;
    /* Adjust with JavaScript */
    height: 9px;
    border-radius: 10px;
}










.playerhud {
    position: absolute;
    right: 10px;
    top: 30px;
}

.playerhudjob {
    white-space: nowrap;
    position: absolute;
    color: white;
    top: 32px;
    left: 65px;
    line-height: unset;
    width: 5.5rem;
    max-width: 5.5rem;
    text-align: start;
    font-size: 0.7rem;
    overflow: hidden;
    text-overflow: ellipsis;
}

.playerhudcash {
    position: absolute;
    color: white;
    top: 33px;
    left: 140px;
    line-height: unset;
    width: 5rem;
    text-align: end;
    font-size: 0.7rem;

}

.playerhudbank {
    position: absolute;
    color: white;
    top: 33px;
    left: 145px;
    line-height: unset;
    width: 5rem;
    text-align: end;
    font-size: 0.7rem;
    display: none;
}

.playercashimg {
    position: absolute;
    top: 26px;
    display: none;
    left: 225px;

}

.playerbankimg {
    position: absolute;
    top: 30px;
    left: 230px;
    display: none;


}


@media (width: 2560px) and (height: 1440px) {



    .allhudmicontextwalk {
        position: absolute;
        width: 0.8vh;
        height: 1.5vh;
        bottom: 2.9vh;
        left: 28vh;
        z-index: 100;
        display: none;

    }

    .allhudmicontext {
        position: absolute;
        width: 0.9vh;
        height: 1.5vh;
        bottom: 2.1vh;
        left: 15.57vh;
        z-index: 100;
        display: none;
    }

    .text-hud-map-walk {
        position: absolute;
        width: 29rem !important;
        height: 7rem !important;
        bottom: 0rem;
        left: 0.35vh;
    }



    .text-hud-icons-onfoot .text-hud-health2 {
        position: absolute;
        font-size: 0.8vh;
        flex: 1;
        left: 2.1vh;
        bottom: 0.7vh;
        width: 3vh;
        text-align: center;
    }


    .text-hud-icons-onfoot .micbar-text {
        position: absolute;
        font-size: 0.8vh;
        flex: 1;
        left: 24.2vh;
        bottom: 0.7vh;

    }

    .text-hud-icons-onfoot .text-hud-armor2 {
        position: absolute;
        font-size: 0.8vh;
        flex: 1;
        left: 5.7vh;
        bottom: 0.7vh;
        width: 3vh;
        text-align: center;
    }

    .text-hud-icons-onfoot .text-hud-water2 {
        position: absolute;
        font-size: 0.8vh;
        flex: 1;
        left: 13vh;
        bottom: 0.7vh;
        width: 3vh;
        text-align: center;
    }

    .text-hud-icons-onfoot .text-hud-hunger {
        position: absolute;
        font-size: 0.8vh;
        flex: 1;
        left: 1.5vh;
        bottom: 0.2vh;
        width: 3vh;
        text-align: center;
    }

    .text-hud-icons-onfoot .text-hud-stress2 {
        position: absolute;
        font-size: 0.8vh;
        flex: 1;
        left: 9.4vh;
        bottom: 0.7vh;
        width: 3vh;
        text-align: center;
    }

    .text-hud-icons-onfoot .text-hud-stamina {
        position: absolute;
        font-size: 0.8vh;
        flex: 1;
        left: 19.8vh;
        bottom: 0.7vh;
        width: 3vh;
        text-align: center;
    }

    .text-hud-icons-onfoot .text-server-id2 {
        position: absolute;
        font-size: 0.8vh;
        flex: 1;
        left: -0.9vh;
        bottom: 0.7vh;
        width: 3vh;
        text-align: center;
    }

    .text-hud-icons-vehicle .text-hud-health2 {
        position: absolute;
        flex: 1;
        bottom: 2.1vh;
        left: 0.1vh;
        font-size: 0.8vh;
        width: 3vh;
        text-align: center;
    }

    .text-hud-icons-vehicle .text-hud-armor {
        position: absolute;
        flex: 1;
        bottom: 2.1vh;
        left: 4.7vh;
        font-size: 0.8vh;
        width: 3vh;
        text-align: center;
    }

    .text-hud-icons-vehicle .text-hud-water {
        position: absolute;
        flex: 1;
        bottom: 2.1vh;
        left: 13.8vh;
        font-size: 0.8vh;
        width: 3vh;
        text-align: center;
    }

    .text-hud-icons-vehicle .text-hud-hunger {
        position: absolute;
        flex: 1;
        bottom: 2.1vh;
        left: 18.4vh;
        font-size: 0.8vh;
        width: 3vh;
        text-align: center;
    }

    #text-hud-map {
        position: absolute;
        width: 29.9vh !important;
        height: 25.9vh !important;
        bottom: -0.6vh;
        left: 0.6vh;
    }

    .text-hud-icons-vehicle .micbar-text {
        position: absolute;
        left: 10.19vh;
        bottom: 2.3vh;

    }

    .streetnametext {
        position: absolute;
        bottom: 22.7vh;
        left: 5.9vh;
        z-index: 5000;
        color: white;
        font-size: 1.5vh;
    }

    .saattext {
        position: absolute;
        bottom: 22.7vh;
        left: 21vh;
        z-index: 5000;
        color: white;
        font-size: 1.5vh;

    }

    /*--------------- Venice ---------------*/

    .health-bar-walk {
        position: absolute;
        bottom: 1.4vh;
        width: 11.5vh;
        left: 2.1vh;
        height: 18.51vh;
        transform: rotate(180deg);
    }

    .armor-bar-walk {
        position: absolute;
        bottom: 1.4vh;
        width: 11.5vh;
        left: 16.4vh;
        height: 18.51vh;
        -webkit-transform: scaleY(-1);
        transform: scaleY(-1);
    }

    .thirsty-bar-walk {
        position: absolute;
        bottom: -9.1vh;
        width: 11.5vh;
        left: 2.1vh;
        height: 18.51vh;
        -webkit-transform: scaleX(-1);
        transform: scaleX(-1);
        transition: all 0.25s linear;
    }

    .hunger-bar-walk {
        position: absolute;
        bottom: -9.1vh;
        width: 11.5vh;
        left: 16.4vh;
        height: 18.51vh;
        transition: all 0.25s linear;
    }

    .venicemaphud {
        position: absolute;
        width: 29.7vh !important;
        height: 25.6vh !important;
        left: 1.26vh !important;
    }

    .health-bar {
        position: absolute;
        bottom: 2.8vh;
        width: 12.5vh;
        left: 3.2vh;
        height: 18.51vh;
        transform: rotate(180deg);
    }

    .armor-bar {
        position: absolute;
        bottom: 2.8vh;

        width: 12.5vh;
        left: 16.6vh;
        height: 18.51vh;
        -webkit-transform: scaleY(-1);
        transform: scaleY(-1);
    }

    .thirsty-bar {
        position: absolute;
        bottom: 1.75vh;
        width: 12.5vh;
        left: 3.4vh;
        height: 18.51vh;
        -webkit-transform: scaleX(-1);
        transform: scaleX(-1);
        transition: all 0.25s linear;
    }

    .hunger-bar {
        position: absolute;
        bottom: 1.75vh;
        width: 12.5vh;
        left: 16.5vh;
        height: 18.51vh;
        transition: all 0.25s linear;
    }

    .allhudmiconvenice {
        position: absolute;
        width: 1.1vh;
        height: 1.6vh;
        bottom: 2.7vh;
        left: 15.57vh;
        z-index: 100;
        display: none;
    }

    .micbar-venice {
        position: absolute;
        left: 53.01% !important;
        top: 24.35vh;
        transform: translateX(-50%);
        scale: 1.3
    }

    .streetnamevenice {
        position: absolute;
        bottom: 23.4vh;
        left: 6.7vh;
        z-index: 5000;
        color: white;
        font-size: 1.5vh;
    }

    .saatvenice {
        position: absolute;
        bottom: 23.3vh;
        left: 22.vh;
        z-index: 5000;
        color: white;
        font-size: 1.5vh;
    }

















    /* -----------------RADIAL ------------------------*/
    .radial-hud-map-walk {
        position: absolute;
        bottom: -1rem;
        left: 0.35vh;
        width: 29rem;
        height: 7rem;
    }

    .allhudmiconradialwalk {
        position: absolute;
        left: 28.2vh;
        bottom: 2.48vh;
        z-index: 100;
        display: none;
        scale: 1.3
    }

    .health-progress-bar-walk {
        position: absolute;
        left: 5.24rem;
        bottom: 1.9vh;
        height: 3.2vh;
        width: 3.55vh;
    }


    .armor-progress-bar-walk {
        position: absolute;
        left: 8.5rem;
        bottom: 1.6vh;
        height: 3.55vh;
        width: 3.55vh;
    }



    .mic-progress-bar-walk {
        position: absolute;
        left: 24.3rem;
        bottom: 1.6vh;
        height: 3.55vh;
        width: 3.55vh;
    }


    .thirsty-progress-bar-walk {
        position: absolute;
        left: 15.1rem;
        bottom: 1.5vh;
        height: 3.55vh;
        width: 3.55vh;
    }


    .stress-progress-bar-walk {
        position: absolute;
        left: 11.78rem;
        bottom: 1.5vh;
        height: 3.55vh;
        width: 3.55vh;
    }



    .hunger-progress-bar-walk {
        position: absolute;
        left: 18.3rem;
        bottom: 1.5vh;
        height: 3.55vh;
        width: 3.55vh;
    }

    .stamina-progress-bar {
        position: absolute;
        left: 21.3rem;
        bottom: 1.5vh;
        display: none;
        height: 3.55vh;
        width: 3.55vh;
    }


    #radial-hud-map {
        position: absolute;
        width: 27rem;
        height: 23.7rem;
        bottom: -1.6rem;
        left: 1.1vh;
    }

    .health-progress-bar {
        position: absolute;
        left: 4.78rem;
        bottom: 0.75rem;
        height: 3.55vh;
        width: 3.55vh;
        display: none;
    }

    .armor-progress-bar {
        position: absolute;
        left: 8.9rem;
        bottom: 0.75rem;
        height: 3.55vh;
        width: 3.55vh;
        display: none;
    }


    .mic-progress-bar {
        position: absolute;
        left: 13rem;
        bottom: 0.78rem;
        height: 3.55vh;
        width: 3.55vh;
    }

    .radial-id {
        display: flex;
        flex-direction: column;
        position: absolute;
        left: 3.7vh;
        bottom: 0.8vh;
        height: 1.35vh;
        justify-content: center;
        align-items: center;
        width: 1.35vh;
        z-index: 59999;
        text-align: center;
    }

    .thirsty-progress-bar {
        position: absolute;
        left: 17.2rem;
        bottom: 0.75rem;
        height: 3.55vh;
        width: 3.55vh;
        display: none;
    }


    .hunger-progress-bar {
        position: absolute;
        left: 21.3rem;
        bottom: 0.75rem;
        height: 3.55vh;
        width: 3.55vh;
        display: none;
    }

    .saat {
        position: absolute;
        bottom: 19.9vh;
        left: 21.4vh;
        z-index: 5000;
        color: white;
        font-size: 1.5vh;

    }

    .streetname {
        position: absolute;
        bottom: 19.9vh;
        left: 6.5vh;
        z-index: 5000;
        color: white;
        font-size: 1.5vh;
    }

    .allhudmiconradial {
        position: absolute;
        left: 15.7vh;
        bottom: 1.8vh;
        z-index: 100;
        display: block;
        width: 0.80vh;
        height: 1.4vh;
        scale: 1.1;
    }
}

@media (width: 1768px) and (height: 992px) {



    .allhudmicontextwalk {
        position: absolute;
        width: 0.8vh;
        height: 1.5vh;
        bottom: 2.9vh;
        left: 27.99vh;
        z-index: 100;
        display: none;
    }





    .text-hud-icons-onfoot .text-hud-health2 {
        position: absolute;
        font-size: 0.8vh;
        flex: 1;
        left: 2.1vh;
        bottom: 0.7vh;
        width: 3vh;
        text-align: center;
    }


    .text-hud-icons-onfoot .micbar-text {
        position: absolute;
        font-size: 0.8vh;
        flex: 1;
        left: 24vh;
        bottom: 0.7vh;

    }

    .text-hud-icons-onfoot .text-hud-armor2 {
        position: absolute;
        font-size: 0.8vh;
        flex: 1;
        left: 5.9vh;
        bottom: 0.7vh;
        width: 3vh;
        text-align: center;
    }

    .text-hud-icons-onfoot .text-hud-water2 {
        position: absolute;
        font-size: 0.8vh;
        flex: 1;
        left: 13.1vh;
        bottom: 0.7vh;
        width: 3vh;
        text-align: center;
    }

    .text-hud-icons-onfoot .text-hud-stress2 {
        position: absolute;
        font-size: 0.8vh;
        flex: 1;
        left: 9.4vh;
        bottom: 0.7vh;
        width: 3vh;
        text-align: center;
    }

    .text-hud-icons-onfoot .text-hud-hunger {
        position: absolute;
        font-size: 0.8vh;
        flex: 1;
        left: 1.7vh;
        bottom: 0.2vh;
        width: 3vh;
        text-align: center;
    }

    .text-hud-icons-onfoot .text-hud-stamina {
        position: absolute;
        font-size: 0.8vh;
        flex: 1;
        left: 20vh;
        bottom: 0.7vh;
        width: 3vh;
        text-align: center;
    }

    .text-hud-icons-onfoot .text-server-id2 {
        position: absolute;
        font-size: 0.8vh;
        flex: 1;
        left: -1.2vh;
        bottom: 0.7vh;
        width: 3vh;
        text-align: center;
    }














    .radial-hud-map-walk {
        position: absolute;
        bottom: rem;
        left: 0.35vh;
        width: 23rem;
    }

    .allhudmiconradialwalk {
        position: absolute;
        left: 32.5vh;
        bottom: 1.5vh;
        z-index: 100;
        display: none;
    }

    .health-progress-bar-walk {
        position: absolute;
        left: 4.22rem;
        bottom: 1.5vh;
        height: 3.2vh;
        width: 3.55vh;
    }

    .radial-id-text {
        position: relative;
        bottom: 0.3vh;
        left: -0.6vh;
        color: white;
        font-size: 0.83vh;
    }


    .stress-progress-bar-walk {
        position: absolute;
        left: 9.45rem;
        bottom: 1.1vh;
        height: 3.55vh;
        width: 3.55vh;
    }

    .armor-progress-bar-walk {
        position: absolute;
        left: 6.9rem;
        bottom: 1.1vh;
        height: 3.55vh;
        width: 3.55vh;
    }



    .mic-progress-bar-walk {
        position: absolute;
        left: 19.43rem;
        bottom: 1.1vh;
        height: 3.55vh;
        width: 3.55vh;
    }


    .thirsty-progress-bar-walk {
        position: absolute;
        left: 11.9rem;
        bottom: 1.1vh;
        height: 3.55vh;
        width: 3.55vh;
    }



    .hunger-progress-bar-walk {
        position: absolute;
        left: 14.6rem;
        bottom: 1.0vh;
        height: 3.55vh;
        width: 3.55vh;
    }

    .stamina-progress-bar {
        position: absolute;
        left: 16.99rem;
        bottom: 1.2vh;
        display: none;
        height: 3.55vh;
        width: 3.55vh;
    }


    #radial-hud-map {
        position: absolute;
        width: 18.8rem;
        height: 17.5rem;
        bottom: -2rem;
    }

    .health-progress-bar {
        position: absolute;
        left: 2.65rem;
        bottom: -0.01rem;
        height: 3.55vh;
        width: 3.55vh;
        display: none;
    }

    .armor-progress-bar {
        position: absolute;
        left: 5.6rem;
        bottom: -0.01rem;
        height: 3.55vh;
        width: 3.55vh;
        display: none;
    }

    .mic-progress-bar {
        position: absolute;
        left: 8.38rem;
        bottom: -0.01rem;
        height: 3.55vh;
        width: 3.55vh;
    }

    .thirsty-progress-bar {
        position: absolute;
        left: 11.35rem;
        bottom: -0.01rem;
        height: 3.55vh;
        width: 3.55vh;
        display: none;
    }


    .hunger-progress-bar {
        position: absolute;
        left: 14.15rem;
        bottom: -0.01rem;
        height: 3.55vh;
        width: 3.55vh;
        display: none;
    }

}


@media (width: 1600px) and (height: 1024px) {


    .venicemaphud {
        position: absolute;
        width: 26.2vh !important;
        height: 27vh !important;
    }

    .allhudmiconvenice {
        position: absolute;
        width: 1.1vh;
        height: 1.6vh;
        bottom: 1.45vh;
        left: 12.5vh;
        z-index: 100;
        display: none;
    }

    .health-bar {
        position: absolute;
        bottom: 1.8vh;
        width: 10.5vh;
        left: 1.8vh;
        height: 18.51vh;
        transform: rotate(180deg);
    }



    .hunger-bar {
        position: absolute;
        bottom: 1.5vh;
        width: 10.5vh;
        left: 14vh;
        height: 18.51vh;
        transition: all 0.25s linear;
    }


    .armor-bar {
        position: absolute;
        bottom: 1.8vh;

        width: 10.5vh;
        left: 14vh;
        height: 18.51vh;
        -webkit-transform: scaleY(-1);
        transform: scaleY(-1);
    }

    .thirsty-bar {
        position: absolute;
        bottom: 1.5vh;
        width: 10.5vh;
        left: 2vh;
        height: 18.51vh;
        -webkit-transform: scaleX(-1);
        transform: scaleX(-1);
        transition: all 0.25s linear;
    }

    .micbar-venice {
        position: absolute;
        left: 42f.6% !important;
        top: 24.9vh;
        transform: translateX(-50%);
    }

    .saatvenice {
        position: absolute;
        bottom: 23.3vh;
        left: 17.99vh;
        z-index: 5000;
        color: white;
        font-size: 1.5vh;
    }

    .streetnamevenice {
        position: absolute;
        bottom: 23.4vh;
        left: 4.6vh;
        z-index: 5000;
        color: white;
        font-size: 1.5vh;
    }


    #text-hud-map {
        position: absolute;
        width: 25.9vh !important;
        height: 25.9vh !important;
        bottom: -1vh;
    }

    .saattext {
        position: absolute;
        bottom: 22.3vh;
        left: 16.99vh;
        z-index: 5000;
        color: white;
        font-size: 1.5vh;
    }

    .allhudmicontext {
        position: absolute;
        width: 0.9vh;
        height: 1.5vh;
        bottom: 1.7vh;
        left: 13vh;
        z-index: 100;
        display: none;
    }

    .text-hud-icons-vehicle .micbar-text {
        position: absolute;
        left: 7.5vh;
        bottom: 1.8vh;

    }

    .text-hud-icons-vehicle .text-hud-health2 {
        position: absolute;
        flex: 1;
        bottom: 1.6vh;
        left: -1.4vh;
        font-size: 0.8vh;
        width: 3vh;
        text-align: center;
    }

    .text-hud-icons-vehicle .text-hud-armor2 {
        position: absolute;
        flex: 1;
        bottom: -0vh;
        left: -1.4vh;
        font-size: 0.8vh;
        width: 3vh;
        text-align: center;
    }

    .text-hud-icons-vehicle .text-hud-water2 {
        position: absolute;
        flex: 1;
        bottom: -0vh;
        left: -2.6vh;
        font-size: 0.8vh;
        width: 3vh;
        text-align: center;

    }

    .text-hud-icons-vehicle .text-hud-hunger {
        position: absolute;
        flex: 1;
        bottom: 1.6vh;
        left: 14.5vh;
        font-size: 0.8vh;

        width: 3vh;
        text-align: center;
    }


    .allhudmicontextwalk {
        position: absolute;
        width: 0.8vh;
        height: 1.5vh;
        bottom: 2.8vh;
        left: 27.3vh;
        z-index: 100;
        display: none;
    }



    .text-hud-icons-onfoot .text-hud-health2 {
        position: absolute;
        font-size: 0.8vh;
        flex: 1;
        left: 1.9vh;
        bottom: 0.7vh;
        width: 3vh;
        text-align: center;
    }

    .text-hud-icons-onfoot .text-hud-stress2 {
        position: absolute;
        font-size: 0.8vh;
        flex: 1;
        left: 9vh;
        bottom: 0.7vh;
        width: 3vh;
        text-align: center;
    }

    .text-hud-icons-onfoot .micbar-text {
        position: absolute;
        font-size: 0.8vh;
        flex: 1;
        left: 23.3vh;
        bottom: 0.7vh;

    }

    .text-hud-icons-onfoot .text-hud-armor2 {
        position: absolute;
        font-size: 0.8vh;
        flex: 1;
        left: 5.5vh;
        bottom: 0.7vh;
        width: 3vh;
        text-align: center;
    }

    .text-hud-icons-onfoot .text-hud-water2 {
        position: absolute;
        font-size: 0.8vh;
        flex: 1;
        left: 12.5vh;
        bottom: 0.7vh;
        width: 3vh;
        text-align: center;
    }

    .text-hud-icons-onfoot .text-hud-hunger2 {
        position: absolute;
        font-size: 0.8vh;
        flex: 1;
        left: 16.1vh;
        bottom: 0.7vh;
        width: 3vh;
        text-align: center;
    }

    .text-hud-icons-onfoot .text-hud-stamina2 {
        position: absolute;
        font-size: 0.8vh;
        flex: 1;
        left: 1.1vh;
        bottom: 0.2vh;
        width: 3vh;
        text-align: center;
    }

    .text-hud-icons-onfoot .text-server-id2 {
        position: absolute;
        font-size: 1vh;
        flex: 1;
        left: -1.3vh;
        bottom: 0.5vh;

        width: 3vh;
        text-align: center;
    }


    .radial-hud-map-walk {
        position: absolute;
        bottom: -1rem;
        left: 0.35vh;
        width: 23rem;
    }

    .allhudmiconradialwalk {
        position: absolute;
        left: 31.4vh;
        bottom: 1.6vh;
        z-index: 100;
        display: none;
    }

    .allhudmiconradial {
        position: absolute;
        left: 12.9vh;
        bottom: 0.5vh;
        z-index: 100;
        display: block;
    }

    .saat {
        position: absolute;
        bottom: 19.5vh;
        left: 18vh;
        z-index: 5000;
        color: white;
        font-size: 1.5vh;

    }

    .streetname {
        position: absolute;
        bottom: 19.5vh;
        left: 5vh;
        z-index: 5000;
        color: white;
        font-size: 1.5vh;
    }

    .health-progress-bar-walk {
        position: absolute;
        left: 4.25rem;
        bottom: 1.4vh;
        height: 3.2vh;
        width: 3.55vh;
    }

    .stress-progress-bar-walk {
        position: absolute;
        left: 9.45rem;
        bottom: 1.0vh;
        height: 3.55vh;
        width: 3.55vh;
    }

    .armor-progress-bar-walk {
        position: absolute;
        left: 6.95rem;
        bottom: 1.1vh;
        height: 3.55vh;
        width: 3.55vh;
    }



    .mic-progress-bar-walk {
        position: absolute;
        left: 19.4rem;
        bottom: 1.0vh;
        height: 3.55vh;
        width: 3.55vh;
    }


    .thirsty-progress-bar-walk {
        position: absolute;
        left: 12rem;
        bottom: 1.1vh;
        height: 3.55vh;
        width: 3.55vh;
    }



    .hunger-progress-bar-walk {
        position: absolute;
        left: 14.65rem;
        bottom: 1.0vh;
        height: 3.55vh;
        width: 3.55vh;
    }

    .stamina-progress-bar {
        position: absolute;
        left: 17rem;
        bottom: 1.0vh;
        display: none;
        height: 3.55vh;
        width: 3.55vh;
    }


    #radial-hud-map {
        position: absolute;
        width: 17rem;
        height: 17.5rem;
        bottom: -2rem;
    }

    .health-progress-bar {
        position: absolute;
        left: 2.3rem;
        bottom: -0.01rem;
        height: 3.55vh;
        width: 3.55vh;
        display: none;
    }

    .armor-progress-bar {
        position: absolute;
        left: 4.9rem;
        bottom: -0.01rem;
        height: 3.55vh;
        width: 3.55vh;
        display: none;
    }

    .mic-progress-bar {
        position: absolute;
        left: 7.45rem;
        bottom: -0.01rem;
        height: 3.55vh;
        width: 3.55vh;
    }

    .thirsty-progress-bar {
        position: absolute;
        left: 10.1rem;
        bottom: -0.01rem;
        height: 3.55vh;
        width: 3.55vh;
        display: none;
    }


    .hunger-progress-bar {
        position: absolute;
        left: 12.65rem;
        bottom: -0.01rem;
        height: 3.55vh;
        width: 3.55vh;
        display: none;
    }

    .radial-id-text {
        position: absolute;
        bottom: 0.5vh;
        left: -.0vh;
        color: white;
        font-size: 0.83vh;
    }

}

@media (width: 1680px) and (height: 1050px) {

    .venicemaphud {
        position: absolute;
        width: 27.2vh !important;
        height: 27vh !important;
    }

    .allhudmiconvenice {
        position: absolute;
        width: 1.1vh;
        height: 1.6vh;
        bottom: 1.45vh;
        left: 13vh;
        z-index: 100;
        display: none;
    }

    .health-bar {
        position: absolute;
        bottom: 1.8vh;
        width: 10.5vh;
        left: 1.8vh;
        height: 18.51vh;
        transform: rotate(180deg);
    }



    .hunger-bar {
        position: absolute;
        bottom: 1.5vh;
        width: 10.5vh;
        left: 15vh;
        height: 18.51vh;
        transition: all 0.25s linear;
    }


    .armor-bar {
        position: absolute;
        bottom: 1.8vh;

        width: 10.5vh;
        left: 15vh;
        height: 18.51vh;
        -webkit-transform: scaleY(-1);
        transform: scaleY(-1);
    }

    .thirsty-bar {
        position: absolute;
        bottom: 1.5vh;
        width: 10.5vh;
        left: 2vh;
        height: 18.51vh;
        -webkit-transform: scaleX(-1);
        transform: scaleX(-1);
        transition: all 0.25s linear;
    }

    .micbar-venice {
        position: absolute;
        left: 44.6% !important;
        top: 24.9vh;
        transform: translateX(-50%);
    }

    .saatvenice {
        position: absolute;
        bottom: 23.3vh;
        left: 18.99vh;
        z-index: 5000;
        color: white;
        font-size: 1.5vh;
    }

    .streetnamevenice {
        position: absolute;
        bottom: 23.4vh;
        left: 4.6vh;
        z-index: 5000;
        color: white;
        font-size: 1.5vh;
    }





    #text-hud-map {
        position: absolute;
        width: 26.9vh !important;
        height: 25.9vh !important;
        bottom: -1vh;
    }

    .saattext {
        position: absolute;
        bottom: 22.3vh;
        left: 17.99vh;
        z-index: 5000;
        color: white;
        font-size: 1.5vh;
    }

    .allhudmicontext {
        position: absolute;
        width: 0.9vh;
        height: 1.5vh;
        bottom: 1.7vh;
        left: 13.5vh;
        z-index: 100;
        display: none;
    }

    .text-hud-icons-vehicle .micbar-text {
        position: absolute;
        left: 8.0vh;
        bottom: 1.8vh;

    }

    .text-hud-icons-vehicle .text-hud-health2 {
        position: absolute;
        flex: 1;
        bottom: 1.6vh;
        left: -1.2vh;
        font-size: 0.8vh;
        width: 3vh;
        text-align: center;
    }

    .text-hud-icons-vehicle .text-hud-armor2 {
        position: absolute;
        flex: 1;
        bottom: -0.0vh;
        left: -1vh;
        font-size: 0.8vh;
        width: 3vh;
        text-align: center;
    }

    .text-hud-icons-vehicle .text-hud-water2 {
        position: absolute;
        flex: 1;
        bottom: 0.1vh;
        left: -1.7vh;
        font-size: 0.8vh;
        width: 3vh;
        text-align: center;
    }

    .text-hud-icons-vehicle .text-hud-hunger2 {
        position: absolute;
        flex: 1;
        bottom: -0vh;
        left: -2.4vh;
        font-size: 0.8vh;
    }









    .allhudmicontextwalk {
        position: absolute;
        width: 0.8vh;
        height: 1.5vh;
        bottom: 2.8vh;
        left: 26.5vh;
        z-index: 100;
        display: none;
    }

    .text-hud-icons-onfoot .text-hud-health2 {
        position: absolute;
        font-size: 0.8vh;
        flex: 1;
        left: 1.8vh;
        bottom: 0.5vh;
        width: 3vh;
        text-align: center;
    }

    .text-hud-icons-onfoot .text-hud-stress2 {
        position: absolute;
        font-size: 0.8vh;
        flex: 1;
        left: 8.6vh;
        bottom: 0.5vh;
        width: 3vh;
        text-align: center;
    }


    .text-hud-icons-onfoot .micbar-text {
        position: absolute;
        font-size: 0.8vh;
        flex: 1;
        left: 22.6vh;
        bottom: 0.7vh;

    }

    .text-hud-icons-onfoot .text-hud-armor2 {
        position: absolute;
        font-size: 0.8vh;
        flex: 1;
        left: 5.3vh;
        bottom: 0.5vh;
        width: 3vh;
        text-align: center;
    }

    .text-hud-icons-onfoot .text-hud-water2 {
        position: absolute;
        font-size: 0.8vh;
        flex: 1;
        left: 12.2vh;
        bottom: 0.5vh;
        width: 3vh;
        text-align: center;
    }

    .text-hud-icons-onfoot .text-hud-hunger2 {
        position: absolute;
        font-size: 0.8vh;
        flex: 1;
        left: 15.6vh;
        bottom: 0.5vh;
        width: 3vh;
        text-align: center;
    }

    .text-hud-icons-onfoot .text-hud-stamina2 {
        position: absolute;
        font-size: 0.8vh;
        flex: 1;
        left: 0.5vh;
        bottom: 0vh;
        width: 3vh;
        text-align: center;
    }

    .text-hud-icons-onfoot .text-server-id2 {
        position: absolute;
        font-size: 0.8vh;
        flex: 1;
        left: -1.4vh;
        bottom: 0.5vh;
        width: 3vh;
        text-align: center;
    }
















    .radial-hud-map-walk {
        position: absolute;
        bottom: -1rem;
        left: 0.35vh;
        width: 23rem;
    }

    .allhudmiconradialwalk {
        position: absolute;
        left: 30.8vh;
        bottom: 1.3vh;
        z-index: 100;
        display: none;
    }

    .allhudmiconradial {
        position: absolute;
        left: 13.2vh;
        bottom: 0.5vh;
        z-index: 100;
        display: block;
    }

    .saat {
        position: absolute;
        bottom: 19.5vh;
        left: 18vh;
        z-index: 5000;
        color: white;
        font-size: 1.5vh;

    }

    .streetname {
        position: absolute;
        bottom: 19.5vh;
        left: 5vh;
        z-index: 5000;
        color: white;
        font-size: 1.5vh;
    }

    .health-progress-bar-walk {
        position: absolute;
        left: 4.24rem;
        bottom: 1.3vh;
        height: 3.2vh;
        width: 3.55vh;
    }


    .armor-progress-bar-walk {
        position: absolute;
        left: 6.9rem;
        bottom: 0.9vh;
        height: 3.55vh;
        width: 3.55vh;
    }



    .mic-progress-bar-walk {
        position: absolute;
        left: 19.4rem;
        bottom: 0.9vh;
        height: 3.55vh;
        width: 3.55vh;
    }


    .thirsty-progress-bar-walk {
        position: absolute;
        left: 12rem;
        bottom: 0.9vh;
        height: 3.55vh;
        width: 3.55vh;
    }

    .stress-progress-bar-walk {
        position: absolute;
        left: 14.40vh;
        bottom: 0.9vh;
        height: 3.55vh;
        width: 3.55vh;
    }

    .hunger-progress-bar-walk {
        position: absolute;
        left: 14.6rem;
        bottom: 0.9vh;
        height: 3.55vh;
        width: 3.55vh;
    }

    .stamina-progress-bar {
        position: absolute;
        left: 16.99rem;
        bottom: 0.9vh;
        display: none;
        height: 3.55vh;
        width: 3.55vh;
    }


    #radial-hud-map {
        position: absolute;
        width: 18rem;
        height: 18rem;
        bottom: -2rem;
    }

    .health-progress-bar {
        position: absolute;
        left: 2.42rem;
        bottom: 0.05rem;
        height: 3.55vh;
        width: 3.55vh;
        display: none;
    }

    .armor-progress-bar {
        position: absolute;
        left: 5.2rem;
        bottom: 0.05rem;
        height: 3.55vh;
        width: 3.55vh;
        display: none;
    }

    .mic-progress-bar {
        position: absolute;
        left: 7.9rem;
        bottom: 0.05rem;
        height: 3.55vh;
        width: 3.55vh;
    }

    .thirsty-progress-bar {
        position: absolute;
        left: 10.7rem;
        bottom: 0.05rem;
        height: 3.55vh;
        width: 3.55vh;
        display: none;
    }


    .hunger-progress-bar {
        position: absolute;
        left: 13.4rem;
        bottom: 0.05rem;
        height: 3.55vh;
        width: 3.55vh;
        display: none;
    }

    .radial-id-text {
        position: absolute;
        bottom: 0.5vh;
        left: -0.1vh;

        color: white;
        font-size: 0.83vh;
    }
}




@media (width: 1600px) and (height: 900px) {


    .allhudmicontextwalk {
        position: absolute;
        width: 0.8vh;
        height: 1.5vh;
        bottom: 3.5vh;
        left: 31vh;
        z-index: 100;
        display: none;
    }

    .text-hud-icons-onfoot .text-hud-health2 {
        position: absolute;
        font-size: 1vh;
        flex: 1;
        left: 2.8vh;
        bottom: 0.9vh;
        width: 3vh;
        text-align: center;
    }

    .text-hud-icons-onfoot .text-hud-stress2 {
        position: absolute;
        font-size: 1vh;
        flex: 1;
        left: 10.9vh;
        bottom: 0.9vh;
        width: 3vh;
        text-align: center;
    }

    .text-hud-icons-onfoot .micbar-text {
        position: absolute;
        font-size: 1vh;
        flex: 1;
        left: 27vh;
        bottom: 1vh;

    }

    .text-hud-icons-onfoot .text-hud-armor2 {
        position: absolute;
        font-size: 1vh;
        flex: 1;
        left: 7.0vh;
        bottom: 0.9vh;
        width: 3vh;
        text-align: center;
    }

    .text-hud-icons-onfoot .text-hud-water2 {
        position: absolute;
        font-size: 1vh;
        flex: 1;
        left: 15.0vh;
        bottom: 0.9vh;
        width: 3vh;
        text-align: center;
    }

    .text-hud-icons-onfoot .text-hud-hunger2 {
        position: absolute;
        font-size: 1vh;
        flex: 1;
        left: 19vh;
        bottom: 0.9vh;
        width: 3vh;
        text-align: center;
    }

    .text-hud-icons-onfoot .text-hud-stamina {
        position: absolute;
        font-size: 1vh;
        flex: 1;

        left: 22.6vh;
        bottom: 0.9vh;

    }

    .text-hud-icons-onfoot .text-server-id2 {
        position: absolute;
        font-size: 1vh;
        flex: 1;
        left: -0.8vh;
        bottom: 1vh;
        width: 3vh;
        text-align: center;
    }



    .radial-hud-map-walk {
        position: absolute;
        bottom: -1rem;
        left: 0.35vh;
        width: 23rem;
    }

    .allhudmiconradialwalk {
        position: absolute;
        left: 35.8vh;
        bottom: 1.7vh;
        z-index: 100;
        display: none;
    }

    .allhudmiconradial {
        position: absolute;
        left: 14.5vh;
        bottom: 0.5vh;
        z-index: 100;
        display: block;
    }

    .saat {
        position: absolute;
        bottom: 19.8vh;
        left: 20.5vh;
        z-index: 5000;
        color: white;
        font-size: 1.5vh;

    }

    .streetname {
        position: absolute;
        bottom: 19.9vh;
        left: 6vh;
        z-index: 5000;
        color: white;
        font-size: 1.5vh;
    }

    .health-progress-bar-walk {
        position: absolute;
        left: 4.3rem;
        bottom: 1.9vh;
        height: 3.2vh;
        width: 3.55vh;
    }

    .stress-progress-bar-walk {
        position: absolute;
        left: 9.5rem;
        bottom: 1.5vh;
        height: 3.55vh;
        width: 3.55vh;
    }

    .armor-progress-bar-walk {
        position: absolute;
        left: 7rem;
        bottom: 1.7vh;
        height: 3.55vh;
        width: 3.55vh;
    }



    .mic-progress-bar-walk {
        position: absolute;
        left: 19.5rem;
        bottom: 1.5vh;
        height: 3.55vh;
        width: 3.55vh;
    }


    .thirsty-progress-bar-walk {
        position: absolute;
        left: 12.1rem;
        bottom: 1.5vh;
        height: 3.55vh;
        width: 3.55vh;
    }



    .hunger-progress-bar-walk {
        position: absolute;
        left: 14.7rem;
        bottom: 1.5vh;
        height: 3.55vh;
        width: 3.55vh;
    }

    .stamina-progress-bar {
        position: absolute;
        left: 17.08rem;
        bottom: 1.5vh;
        display: none;
        height: 3.55vh;
        width: 3.55vh;
    }


    #radial-hud-map {
        position: absolute;
        width: 17rem;
        height: 16rem;
        bottom: -2rem;
    }

    .health-progress-bar {
        position: absolute;
        left: 2.38rem;
        bottom: 0.02rem;
        height: 3.55vh;
        width: 3.55vh;
        display: none;
    }

    .armor-progress-bar {
        position: absolute;
        left: 5rem;
        bottom: 0.02rem;
        height: 3.55vh;
        width: 3.55vh;
        display: none;
    }

    .mic-progress-bar {
        position: absolute;
        left: 7.6rem;
        bottom: -0.01rem;
        height: 3.55vh;
        width: 3.55vh;
    }

    .thirsty-progress-bar {
        position: absolute;
        left: 10.2rem;
        bottom: -0.01rem;
        height: 3.55vh;
        width: 3.55vh;
        display: none;
    }


    .hunger-progress-bar {
        position: absolute;
        left: 12.8rem;
        bottom: -0.01rem;
        height: 3.55vh;
        width: 3.55vh;
        display: none;
    }

    .radial-id-text {
        position: relative;
        bottom: -2.8vh;
        left: -.0vh;
        color: white;
        font-size: 0.83vh;
    }


    .radial-id {
        display: flex;
        flex-direction: column;
        position: absolute;
        left: 4.35vh;
        bottom: 3.8vh;
        height: 1.35vh;
        justify-content: center;
        align-items: center;
        width: 1.35vh;
        z-index: 59999;
    }

}






@media (width: 1366px) and (height: 768px) {





    .allhudmicontextwalk {
        position: absolute;
        width: 1vh;
        height: 2vh;
        bottom: 4.3vh;
        left: 36.1vh;
        z-index: 100;
        display: none;
    }

    .allhudmicontext {
        position: absolute;
        width: 0.9vh;
        height: 1.5vh;
        bottom: 1.8vh;
        left: 15vh;

        z-index: 100;
        display: none;
    }

    .text-hud-icons-onfoot .text-hud-health2 {
        position: absolute;
        font-size: 1vh;
        flex: 1;
        left: 4vh;
        bottom: 1.5vh;
        width: 3vh;
        text-align: center;
    }

    .text-hud-icons-vehicle .micbar-text {
        position: absolute;
        left: 9.35vh;
        bottom: 1.8vh;
        width: 3vh;
        text-align: center;
    }

    .text-hud-icons-vehicle .text-hud-health2 {
        position: absolute;
        flex: 1;
        bottom: 1.6vh;
        left: 0h;
        font-size: 0.8vh;
        width: 3vh;
        text-align: center;
    }

    .text-hud-icons-onfoot .text-hud-stress2 {
        position: absolute;
        font-size: 1vh;
        flex: 1;
        left: 13.5vh;
        bottom: 1.3vh;
        width: 3vh;
        text-align: center;
    }

    .text-hud-icons-vehicle .text-hud-armor2 {
        position: absolute;
        flex: 1;
        bottom: .2vh;
        left: 0vh;
        font-size: 0.8vh;
        width: 3vh;
        text-align: center;
    }

    .text-hud-icons-vehicle .text-hud-water2 {
        position: absolute;
        flex: 1;
        bottom: .2vh;
        left: 0vh;
        font-size: 0.8vh;
        width: 3vh;
        text-align: center;
    }

    .text-hud-icons-vehicle .text-hud-hunger2 {
        position: absolute;
        flex: 1;
        bottom: .2vh;
        left: 0vh;
        font-size: 0.8vh;
        width: 3vh;
        text-align: center;
    }

    .text-hud-icons-onfoot .micbar-text {
        position: absolute;
        font-size: 1vh;
        flex: 1;
        left: 32.2vh;
        bottom: 1.5vh;

    }

    .text-hud-icons-onfoot .text-hud-armor2 {
        position: absolute;
        font-size: 1vh;
        flex: 1;
        left: 8.9vh;
        bottom: 1.5vh;
        width: 3vh;
        text-align: center;
    }

    .text-hud-icons-onfoot .text-hud-water2 {
        position: absolute;
        font-size: 1vh;
        flex: 1;
        left: 18.3vh;
        bottom: 1.5vh;
        width: 3vh;
        text-align: center;
    }

    .text-hud-icons-onfoot .text-hud-hunger2 {
        position: absolute;
        font-size: 1vh;
        flex: 1;
        left: 23vh;
        bottom: 1.5vh;
        width: 3vh;
        text-align: center;
    }

    .text-hud-icons-onfoot .text-hud-stamina {
        position: absolute;
        font-size: 1vh;
        flex: 1;
        left: 27.2vh;
        bottom: 1.5vh;

    }

    .text-hud-icons-onfoot .text-server-id2 {
        position: absolute;
        font-size: 1vh;
        flex: 1;
        left: -.2vh;
        bottom: 1.5vh;
        width: 3vh;
        text-align: center;
    }










    .radial-hud-map-walk {
        position: absolute;
        bottom: -1rem;
        left: 0.35vh;
        width: 19.5rem;
    }

    .allhudmiconradialwalk {
        position: absolute;
        left: 35.4vh;
        bottom: 1.3vh;
        z-index: 100;
        display: none;
    }

    .allhudmiconradial {
        position: absolute;
        left: 14.5vh;
        bottom: 0.5vh;
        z-index: 100;
        display: block;
    }

    .saat {
        position: absolute;
        bottom: 19.9vh;
        left: 20.5vh;
        z-index: 5000;
        color: white;
        font-size: 1.5vh;

    }

    .streetname {
        position: absolute;
        bottom: 19.9vh;
        left: 6vh;
        z-index: 5000;
        color: white;
        font-size: 1.5vh;
    }

    .health-progress-bar-walk {
        position: absolute;
        left: 3.65rem;
        bottom: 1.7vh;
        height: 3.2vh;
        width: 3.55vh;
    }


    .armor-progress-bar-walk {
        position: absolute;
        left: 5.9rem;
        bottom: 1.4vh;
        height: 3.55vh;
        width: 3.55vh;
    }



    .mic-progress-bar-walk {
        position: absolute;
        left: 16.5rem;
        bottom: 1.3vh;
        height: 3.55vh;
        width: 3.55vh;
    }


    .thirsty-progress-bar-walk {
        position: absolute;
        left: 10.3rem;
        bottom: 1.4vh;
        height: 3.55vh;
        width: 3.55vh;
    }



    .hunger-progress-bar-walk {
        position: absolute;
        left: 12.5rem;
        bottom: 1.3vh;
        height: 3.55vh;
        width: 3.55vh;
    }

    .stamina-progress-bar {
        position: absolute;
        left: 14.5rem;
        bottom: 1.4vh;
        display: none;
        height: 3.55vh;
        width: 3.55vh;
    }

    .stress-progress-bar-walk {
        position: absolute;
        left: 8.1rem;
        bottom: 1.3vh;
        height: 3.55vh;
        width: 3.55vh;
    }

    #radial-hud-map {
        position: absolute;
        width: 14.5rem;
        height: 13.5rem;
        bottom: -1.5rem;
    }

    .health-progress-bar {
        position: absolute;
        left: 1.99rem;
        bottom: .15rem;
        height: 3.55vh;
        width: 3.55vh;
        display: none;
    }

    .armor-progress-bar {
        position: absolute;
        left: 4.3rem;
        bottom: .15rem;
        height: 3.55vh;
        width: 3.55vh;
        display: none;
    }

    .mic-progress-bar {
        position: absolute;
        left: 6.45rem;
        bottom: .15rem;
        height: 3.55vh;
        width: 3.55vh;
    }

    .thirsty-progress-bar {
        position: absolute;
        left: 8.689rem;
        bottom: .15rem;
        height: 3.55vh;
        width: 3.55vh;
        display: none;
    }


    .hunger-progress-bar {
        position: absolute;
        left: 10.98rem;
        bottom: .15rem;
        height: 3.55vh;
        width: 3.55vh;
        display: none;
    }

    .radial-id-text {
        position: relative;
        bottom: -3.2vh;
        left: 0.3vh;
        color: white;
        font-size: 0.83vh;
    }


    .radial-id {
        display: flex;
        flex-direction: column;
        position: absolute;
        left: 4.35vh;
        bottom: 3.8vh;
        height: 1.35vh;
        justify-content: center;
        align-items: center;
        width: 1.35vh;
        z-index: 59999;
    }

}
</style>