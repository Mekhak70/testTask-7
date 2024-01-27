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
                        <input type="number"/>
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
                <div class="neonmanContener">
                    <img :src="neonmanSrc" alt="neonman" />
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
        background-color: black;
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
        width: 335px;
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
</style>