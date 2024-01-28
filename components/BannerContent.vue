<template>
  <div class="bannerContenetConteiner">
        <div class="bannerContenet">
            <div class="contenet">
                <div class="dataContener">
                    <div class="title">
                        <span>crypto-info</span> founder
                    </div>
                    <div class="text">
                      Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.

                    </div>
                    <div class="changeConterner" >
                    <div class="inputBox">
                        <div class="select">
                            <div class="selectBar">
                                <img :src="BitcoinLogo" alt="Bitcoin"  class="bitcoinIcon"/>
                                <img :src="arrowIcon" alt="Arrow Icon"  class="arrowIcon"/>
                            </div>
                        <select id="cars">
                            <option value="50">50</option>
                            <option value="100">100</option>
                            <option value="150">150</option>
                            <option value="200">200</option>
                        </select>
                    </div>
                    <div style="position: relative;">
                        <span class="dolarIcon">
                            $
                        </span>
                        <input type="number" class="numberInput"/>
                    </div>
                    </div>
                    <div class="criptoBarContener">
                        <div class="criptoBarSection">
                            <div class="criptoBox">
                                <div class="criptoName">
                                    <img :src="BitcoinLogo" alt="Bitcoin"  class="bitcoinIcon"/>
                                    <div class="criptoNameContener">
                                        <span class="criptoNameText">Bitcoin</span>
                                        <span class="criptoShortName">BTC</span>
                                    </div>
                                </div>
                                <div class="criptoPrice">
                                    40046.86
                                </div>

                            </div>
                            <div class="criptoBox">
                                <div class="criptoName">
                                    <img :src="ethereum" alt="Ethereum"  class="bitcoinIcon"/>
                                    <div class="criptoNameContener">
                                        <span class="criptoNameText">Ethereum</span>
                                        <span class="criptoShortName">ETH</span>

                                    </div>


                                </div>
                                <div class="criptoPrice">
                                    2232.25
                                </div>

                            </div>
                        </div>
                        <div class="criptoBarSection">
                            <div class="criptoBox">
                                <div class="criptoName">
                                    <img :src="monero" alt="Monero"  class="bitcoinIcon"/>
                                    <div class="criptoNameContener">
                                        <span class="criptoNameText">Monero</span>
                                        <span class="criptoShortName">XMR</span>

                                    </div>
                                </div>
                                <div class="criptoPrice">
                                    155.70
                                </div>
                            </div>
                            <div class="criptoBox">
                                <div class="criptoName">
                                    <img :src="tron" alt="Tron"  class="bitcoinIcon"/>
                                    <div class="criptoNameContener">
                                        <span class="criptoNameText">Tron</span>
                                        <span class="criptoShortName">TRX</span>

                                    </div>


                                </div>
                                <div class="criptoPrice">
                                    0.11
                                </div>

                            </div>

                        </div>

                    </div>
                </div>
                </div>
                <div class="neonmanContener">
                    <svg class="filter">
                        <filter id="alphaRed">
                            <feColorMatrix mode="matrix" values="1 0 0 0 0  0 0 0 0 0  0 0 0 0 0  0 0 0 1 0" result="joint" />
                        </filter>
                        <filter id="alphaGreen">
                            <feColorMatrix mode="matrix" values="0 0 0 0 0  0 1 0 0 0  0 0 0 0 0  0 0 0 1 0" result="joint" />
                        </filter>
                        <filter id="alphaBlue">
                            <feColorMatrix mode="matrix" values="0 0 0 0 0  0 0 0 0 0  0 0 1 0 0  0 0 0 1 0" result="joint" />
                        </filter>
                        <filter id="alpha">
                            <feColorMatrix type="saturate" values="0"/>
                        </filter>
                        </svg>
                        <div class="imgWrap">
                            <img class="red" :src="neonmanSrc" alt="neonman">
                            <img class="green" :src="neonmanSrc" alt="neonman">
                            <img class="blue" :src="neonmanSrc" alt="neonman">
                        </div>
                </div>
            </div>
        </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      neonmanSrc: require('@/public/blockchain-icons/neonman.svg'),
      BitcoinLogo: require('@/public/blockchain-icons/bitcoinLogo.svg'),
      arrowIcon: require('@/public/icons/arrow.svg'),
      ethereum: require('@/public/blockchain-icons/ethereum.svg'),
      tron: require('@/public/blockchain-icons/tron.svg'),
      monero: require('@/public/blockchain-icons/monero.svg'),

    };
  }
  // Other component options go here
};
</script>

<style>
    .changeConterner{
        display: flex;
        flex-direction: column;
        gap: 40px;
    }
    .bannerContenetConteiner{
        padding-top: 10.5px;
        width: 100%;
        display: flex;
        justify-content: flex-end;

    }
    .bannerContenet{
        display: flex;
        width: 83.17%;
    }
    .contenet{
        width: 85.236%;
        display: flex;
    }
    .dataContener{

        padding-top: 60px;
        color: #FFF;
        width: 45.5%;
        height: 561px;
        display: flex;
        flex-direction: column;
        gap: 40px;
        text-align:  start;

    }
    .neonmanContener{
        width: 54.5%;
        height: 680px;
    }
    .title{
        text-align: start;
        color: #FFF;
        font-family: 'Golos', sans-serif;
        font-size: 114px;
        font-style: normal;
        font-weight: 900;
        line-height: 95px; /* 83.333% */
        text-transform: uppercase;
    }
    .title span {
        white-space: nowrap;
    }
    .text{
        width: 90.426%;
        height: 100px;
        color: var(--Grey-Light, #D0D0D0);
        font-family: 'Golos', sans-serif;
        font-size: 16px;
        font-style: normal;
        font-weight: 400;
        line-height: 25px; /* 156.25% */
    }
    .text span{
        padding-right: 8px;
    }
    .inputBox{
        display: flex;
        gap: 20px;
        z-index: 9999;
    }
    .inputBox select{
        display: flex;
        width: 200px;
        height: 63px;
        padding: 15px 23px;
        justify-content: space-between;
        align-items: center;
        border-radius: 16px;
        background: rgba(255, 255, 255, 0.10);
        color:  #D0D0D0;
        font-family: 'Golos', sans-serif;
        font-size: 18px;
        font-style: normal;
        font-weight: 500;
        line-height: normal;
        border: none;
        outline: none;
        z-index: 99999999999;
    }

    .inputBox input{
        display: flex;
        width: 289px;
        padding: 0 23px;
        height: 63px;
        justify-content: space-between;
        align-items: center;
        border-radius: 16px;
        background: rgba(255, 255, 255, 0.05);
        color:  #D0D0D0;
        font-family: 'Golos', sans-serif;
        font-size: 18px;
        font-style: normal;
        font-weight: 500;
        line-height: normal;
        border: none;
        outline: none;
    }
    .select{
        position: relative;
        width: 200px;
        height: 63px;
        border-radius: 16px;
    }
    .selectBar{
        width: 81px;
        height: 33px;
        position: absolute;
        top: 15px;
        right: 0;
        background-color: rgba(255, 255, 255, );
        display: flex;
        align-items: center;
        gap: 10px;
    }
    .bitcoinIcon{
        width: 33px;
        height: 33px;
    }
    .arrowIcon{
        width: 15px;
        height: 15px;
    }
    select {
    -webkit-appearance: none; /* Disable default arrow in Chrome/Safari */
    -moz-appearance: none; /* Disable default arrow in Firefox */
    appearance: none; /* Disable default arrow in other browsers */
    width: 100%;
    padding: 8px;
    border: 1px solid #ccc;
    border-radius: 4px;
    cursor: pointer;


}

.arrow {
  position: absolute;
  top: 50%;
  right: 10px;
  transform: translateY(-50%);
  pointer-events: none; /* Make sure the div doesn't interfere with select clicks */
}
.dolarIcon{
    position: absolute;
    right: 23px;
    top: 20px;
    color:  #D0D0D0;
    font-family: 'Golos', sans-serif;
    font-size: 18px;
    font-style: normal;
    font-weight: 500;
    line-height: normal;
}
.criptoBarContener{
    width: 470px;
    height: 80px;
    display: flex;
    flex-direction: column;
    gap: 20px;
}
.criptoBarSection{
    display: flex;
    gap: 60px;
}
.criptoBox{
    width: 205px;
    display: flex;
    gap: 20px;
}
.criptoPrice{
    display: flex;
    align-items: center;
    height: 34px;
    color:  #D2D2D2;
    font-family: 'Golos', sans-serif;
    font-size: 18px;
    font-style: normal;
    font-weight: 700;
    line-height: normal;
}
.criptoName{
    display: flex;
    gap: 10px;
}
.criptoNameContener{
    display: flex;
    flex-direction: column;
    gap: 2px;
}
.criptoNameText{
    color:  #D0D0D0;
    font-family: 'Golos', sans-serif;
    font-size: 15px;
    font-style: normal;
    font-weight: 600;
    line-height: normal;
}
.criptoShortName{
    color:  #959595;
    font-family: 'Golos', sans-serif;
    font-size: 12px;
    font-style: normal;
    font-weight: 500;
    line-height: normal;
}
input[type="number"]::-webkit-inner-spin-button,
input[type="number"]::-webkit-outer-spin-button {
  -webkit-appearance: none;
  margin: 0;

}

input[type="number"] {
  -moz-appearance: textfield;

}

.filter{
  display: none;
}



.imgWrap{
  width: 80%;
  height: 80%;
  width: 742.216px;
  height: 680px;
  position: relative;
  overflow: hidden;
  img{
    width: 100%;
    height: 100%;
    object-fit: cover;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%,-50%);
  }
  .red{
    filter: url(#alphaRed);
    mix-blend-mode: lighten;
  }
  .green{
    filter: url(#alphaGreen);
    mix-blend-mode: lighten;
  }
  .blue{
    filter: url(#alphaBlue);
    mix-blend-mode: lighten;
  }
  .text{
    display: block;
    color: #fff;
    font-size: 18px;
    padding: 2px 10px;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%,-50%);
    opacity: 0;
    transition: opacity .3s;
    span{
      position: relative;
      z-index: 1;
    }
    &::before{
      content: "";
      display: block;
      width: 100%;
      height: 100%;
      background-color: #000;
      position: absolute;
      top: 50%;
      left: 50%;
      transform: scale(0,1) translate(-50%,-50%);
      transform-origin: center left;
      transition: transform 0.2s;
      z-index: 0;
    }
  }
  &:hover{
    --time: 0.3s;
    .red{
      transform: translate(-49.5%,-49.8%);
      animation-name: imgGlitch;
      animation-duration: var(--time);
      animation-timing-function: linear;
      animation-iteration-count: infinite;
    }
    .green{
      transform: translate(-50.5%,-48.8%);
      animation-name: imgGlitch;
      animation-duration: var(--time);
      animation-timing-function: linear;
      animation-iteration-count: infinite;
    }
    .blue{
      transform: translate(-50.5%,-50.8%);
      animation-name: imgGlitch;
      animation-duration: var(--time);
      animation-timing-function: linear;
      animation-iteration-count: infinite;
    }
    .text{
      opacity: 1;
      &::before{
        transform: scale(1,1) translate(-50%,-50%);
      }
    }
  }
}

@keyframes imgGlitch {
  0%{
    clip-path: path("371.108,13.5V6.372h-58.145V0H19.68V27.28H0V63.163H50.625V72.933H0.115V80.488H50.625V100.93H11.385V108.22H6.91V147.66H0.115V154.479H6.91V169.173h30.315V189.003H5.125V205.193H2.015V256.377H30.845V291.948H14.675V303.057H56.835V354.557H51.125V405.687H41.185V432.43H230V356.567h-68.205v-12.632h68.205v-17.548h-68.205v-32.905h-20.765v-30.265h69.47v-7.05h60.435v-34.83H46.795v-45.938h38.535ZM104.405,138.294h12.29v30.265h-12.29v-30.265ZM85.725,345.705v-24.342h46.52v17.926H299.48v5.194H85.725Zm56.48-63.653v-8.472H140.53v-16.111h197.455v24.423h-56.18Zm85.073-40.118h-9.102v-4.609h9.102v4.609Zm-9.102-24.423v-18.305h9.102v18.305h-9.102Z");
  }
  50%{
    clip-path: path("M369.1,170.527v-19.359h2.057v-33.98h-2.057v-52.384h-7.64v-7.62H127.965v-5.782h104.41v-79.563H177.35v-5.741h17.29v-20.924h52.155V0H74.925v4.73H0V13.984H19.98v35.575H0.73v54.22H19.98v41.74H8.98v9.946h2.045v14.89H5.215v52.384h39.09v1.06H1.755v48.73H23.01v22.778H64.575v3.997h3.98v8.036h-3.994v-8.036H0.87v19.27H73.42v22.423h-34.76v16.603H114.53v12.746H22.24v22.423H41.57v12.88h46.865v9.536H8.59v26.34H68.855v30.957h-36.175v17.538h63.52v8.264H111.95v25.05H183.59v-22.723h119.385v-33.038h20.015v-15.54h-20.015v-48.34h17.305v-45.964h-23.61v-15.33h26.36v-15.32h-26.36v-7.207h26.36v-56.468H84.605v-10.034h111.0Zm-188.685-79.15v20.7h-13.295v-20.7h13.295Zm-95.045-51.19h51.43v-7.05h20.605v20.798h-71.035v-13.637Zm81.885,126.51v-8.264h43.265v20.306h-11.025v-16.703h-32.24Zm-61.825,32.928h6.69v7.662h-6.69v-7.662Zm0,24.478h6.69v7.662h-6.69v-7.662Z");
  }
  100% {
    clip-path: path("M371.068,95.328v-19.398H155.197v-11.41h41.88v-8.41h92.006V24.963h-27.707V4.831H89.49V8.486H29.674V24.9h50.426v9.413H31.806v26.17h-9.567v13.059h-22.493v35.9H16.57v49.183h15.885v23.036H13.86v11.846H2.056v6.689H13.86v36.929h15.79v22.783H12.932v13.207h18.85v9.337H146.18v4.637h143.802v-20.756H200.328v-3.831h23.877v-4.536h-23.877v-16.548h21.027v-15.436h-23.877v-7.122h23.877v-44.057h-13.195v-38.478h13.258V24.963H189.23v-11.886h19.463v-20.033H144.096v-5.644h132.532v-14.55h20.647v-7.752h-20.647v-28.776h18.024v-26.612h-39.718v-5.01h53.53Zm-222.035,173.78v-11.778h116.514v16.248H45.206v4.48H205.31v-10.122h-36.924v-12.366h49.954v17.889H123.25v-12.69h22.465Zm-89.9-95.543v23.495H55.47v-29.007h129.386v5.349h-73.582Z");
  }
}
@media only screen and (max-width: 1470px) {
  .imgWrap {
    width: 680px;
    height: 675px;

  }

}
@media only screen and (max-width: 1366px) {
  .menu ul {
    gap: 20px;
  }
  .imgWrap {
    margin-left: 37px;
    margin-top: 77px;
    width: 630px;
    height: 600px;
}
}

@media only screen and (max-width: 1318px) {

  .imgWrap{
    margin-left: 37px;
    margin-top: 127px;
    width: 580px;
    height: 550px;
}
}
@media only screen and (max-width: 1215px) {

.imgWrap{

    margin-left: 37px;
    margin-top: 159px;
    width: 550px;
    height: 520px;

}
}

@media only screen and (max-width: 1167px) {
  .imgWrap {
    width: 804.296px;
    height: 737px;
    flex-shrink: 0;
  }

  .bannerContenet {
    width: 100%;
    padding: 0 75px 0 70px ;
  }
  .title{
    color: #FFF;
    font-family: Golos;
    font-size: 85px;
    font-style: normal;
    font-weight: 900;
    line-height: 75px; /* 88.235% */
    text-transform: uppercase;
  }
  .bannerContenetConteiner{
    padding-top: 30px;
  }
  .text{
    padding-top: 30px;
    width: 406px;
    color: var(--Grey-Light, #D0D0D0);
    font-family: Golos;
    font-size: 16px;
    font-style: normal;
    font-weight: 400;
    line-height: 25px; /* 156.25% */
  }

  .contenet{
    height: 901px;
    position: absolute;
    z-index: 999;

  }
  .criptoBarContener{
    height: 411px;

  }
  .changeConterner{

padding-top: 50px;
display: flex;
justify-content: space-between;
flex-direction: column-reverse;

}
  .dataContener{

    gap: 0;
  }
  .criptoBarSection{
    display: flex;
    flex-direction: column;
    gap: 30px;
}
.neonmanContener{
    position: absolute;
    z-index: 0;
    right: -100px;
    margin-top: 180px;
    box-sizing: border-box;
    width: 580px;
    height: 770px;
    flex-shrink: 0;
    overflow: hidden;
    z-index: 9999;
    /* right: -100px; */

    }
    .imgWrap img{
        position: absolute;
        z-index: 0;
        overflow: hidden;
    }

  .inputBox{
    position: absolute;
    z-index:9999999;
  }

  .card{
        display: flex;
        width: 100%;
        padding: 20px;
        align-items: flex-start;
        gap: 10px;
        border-radius: 14px;
        background: #171520;
        box-shadow: 0px 0px 35px 0px rgba(0, 0, 0, 0.15);
    }


}


@media only screen and (max-width: 1150px) {
    .neonmanContener{
      width: 570px;
      right: -95px;
    }
}
@media only screen and (max-width: 1100px) {
    .neonmanContener{
      right: -88px;
    }
}
@media only screen and (max-width: 1050px) {
    .neonmanContener{
      right: -80px;
    }
}
@media only screen and (max-width: 1020px) {
    .neonmanContener{
      right: -75px;
    }
}
@media only screen and (max-width: 1000px) {
    .neonmanContener{
      right: -73px;
    }
}
@media only screen and (max-width: 965px) {
    .neonmanContener{
      right: -69px;
    }
}
@media only screen and (max-width: 950px) {
    .neonmanContener{
      right: -63px;
    }
}
@media only screen and (max-width: 900px) {
    .neonmanContener{
      right: -56px;
    }
}
@media only screen and (max-width: 875px) {
    .neonmanContener{
      right: -54px;
    }
}
@media only screen and (max-width: 850px) {
    .neonmanContener{
      right: -52px;
    }
}
@media only screen and (max-width: 825px) {
    .neonmanContener{
      right: -48px;
    }
}
@media only screen and (max-width: 800px) {
    .neonmanContener{
      right: -43px;
    }
}
@media only screen and (max-width: 750px) {
    .neonmanContener{
      right: -40px;
    }
}
@media only screen and (max-width: 743px) {
  .inputBox {
    position: static;

}
  .neonmanContener{
    display: none;
  }
  .cards-container{
    padding: 20px;
  }
  .card{
    display: flex;

    width: 350px;

    flex-direction: column;
    align-items: center;
    gap: 10px;
  }
  .bannerContenet{
    padding: 0 20px;
  }
  .dataContener{
    width: 100%;
    padding-top: 0;
  }
  .title{
    color: #FFF;
    font-family: Golos;
    font-size: 71px;
    font-style: normal;
    font-weight: 900;
    line-height: 65px; /* 91.549% */
    text-transform: uppercase;
  }
  .title span{
    white-space: wrap;
 }
.text{
    width: 100%;
    color: var(--Grey-Light, #D0D0D0);
    font-family: Golos;
    font-size: 14px;
    font-style: normal;
    font-weight: 400;
    line-height: 22px; /* 157.143% */
    padding-top: 20px;
}
.changeConterner{
    padding-top:25px;
}
.criptoBarContener{
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 20px;
    align-self: stretch;
}
.criptoBarContener{
    height: 196px;
}
.criptoBarSection{
    gap: 20px;
}
.inputBox{
        display: flex;
        flex-direction: column;
        gap: 20px;
        z-index: 9999;
    }
.inputBox select{
    position: relative;
    width: 100%;
    display: flex;
    height: 57px;
    padding: 15px 23px;
    justify-content: space-between;
    align-items: center;
    align-self: stretch;
}
.inputBox{
    width: 100%;
}

.contenet{
  width: calc(97% - 20px);
  height: 705px;
  justify-content: center;
}
.select{
        width: 100%;
    }
    .inputBox input {
       width: 93.2%;
       height: 57px;
    }

}
@media only screen and (max-width: 600px) {
      .inputBox input {
      width: 91.815%;
      height: 57px;
    }
  }

    @media only screen and (max-width: 500px) {
      .inputBox input {
      width: 90.108%;
      height: 57px;


    }

  }
    @media only screen and (max-width: 390px) {
      .inputBox input {
      height: 57px;
      width: 87.108%;

    }
  }
</style>