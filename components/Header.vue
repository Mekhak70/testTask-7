<template>
  <div class="header">
    <div class="logo">
      <div class="hamburgerMenu" >
        <img :src="menuBarSrc" alt="Hamburger icon" />
      </div>

      <img :src="logoSrc" alt="Logo" class="logoImg" />
    </div>
<div class="hamburger-menu">

    <input id="menu__toggle" type="checkbox" />
    <label class="menu__btn" for="menu__toggle">
      <div class="menu__btnContener">

        <img :src="logoSrc" alt="Logo" class="logoImg" />

      <div class="closeBatton">X</div>
    </div>
    </label>

    <ul class="menu__box">
      <li><a class="menu__item" href="#">рейтинги</a></li>
      <li><a class="menu__item" href="#">сервисы</a></li>
      <li><a class="menu__item" href="#">обмен</a></li>
      <li><a class="menu__item" href="#">отзывы</a></li>
      <li><a class="menu__item" href="#">FAQ</a></li>
      <li><a class="menu__item" href="#">о нас</a></li>
      <li><a class="menu__item" href="#">контакты</a></li>
      <div class="setCont">
      <span >войти</span>
      <div class="lengSet"><span>RU</span>
        <img :src="arrowSrc" alt="Arrow icon" />
      </div>
    </div>
    </ul>

  </div>


    <div class="menu">
      <ul>
        <li>рейтинги</li>
        <li>сервисы</li>
        <li>обмен</li>
        <li>отзывы</li>
        <li>FAQ</li>
        <li>о нас</li>
        <li>контакты</li>
      </ul>
      <div class="logOut">
        <div>
          <span class="logOutText">войти</span>
        </div>
        <div class="flag">
          <img :src="ruFlagSrc" alt="RU flag" />
          <img :src="arrowSrc" alt="Arrow icon" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      logoSrc: require('@/public/LOGO.svg'),
      ruFlagSrc: require('@/public/icons/ru.svg'),
      arrowSrc: require('@/public/icons/arrow.svg'),
      menuBarSrc: require('@/public/icons/headerBar-icon.svg')
    };
  }
};
</script>


<style>
* {
  padding: 0;
  margin: 0;
}
.hamburgerMenu{
  display: none;
}
.header {
  width: 66.354%;
  height: 40px;
  display: flex;
  justify-content: space-between;
  color: white;
}

.logo {
  display: flex;
  width: 145px;
  height: 40px;
  padding: 1.667px 0.256px 1.03px 0px;
  justify-content: center;
  align-items: center;
  flex-shrink: 0;
}
.setCont{
  display: none;
}
.menu {
  display: flex;
  align-items: center;
  gap: 80px;
}

.menu>ul {
  display: flex;
  gap: 30px;
}

.menu>ul>li {
  list-style: none;
  color: #D0D0D0;
  font-family: 'Golos', sans-serif;
  font-size: 14px;
  font-style: normal;
  font-weight: 500;
  line-height: normal;
  text-transform: uppercase;
}

.logOut {
  display: flex;
  align-items: center;
  gap: 15px;
}

.flag {
  display: flex;
  padding: 12px;
  justify-content: center;
  align-items: center;
  gap: 8px;
  border-radius: 11px;
  background: rgba(255, 255, 255, 0.10);
}

.flag span {
  color:  #D0D0D0;
  font-family: "Font Awesome 6 Free";
  font-size: 12px;
  font-style: normal;
  font-weight: 900;
  line-height: 15px;
  text-transform: uppercase;
}
.hamburger-menu{
  display: none;
}
@media only screen and (max-width: 1450px) {
  .menu{
    gap: 40px;
  }
}
@media only screen and (max-width: 1167px) {
  .hamburger-menu{
  display: flex;
}

  .menu ul {
    display: none;
  }


  .header {
   width: 100%;
  }

  .logOutText {
    color: var(--Grey-Light, #D0D0D0); /* Make sure --Grey-Light is defined and has a valid value */
    font-family: Golos;
    font-size: 14px;
    font-style: normal;
    font-weight: 500;
    line-height: normal;
    text-transform: uppercase;
  }
  .hamburgerMenu{
    display: flex;
    padding: 14px;
    align-items: flex-start;
    gap: 10px;
    border-radius: 11px;
    background: rgba(255, 255, 255, 0.10);
  }
  .logo{
    padding-left: 70px;
    display: flex;
    width: 334.5px;
    justify-content: flex-start;
    align-items: center;
    gap: 30px;
    flex-shrink: 0;
  }
  .logOut{
    padding-right: 70px;
  }
  .logoImg{
    width: 144.744px;
    height: 37.303px;
    flex-shrink: 0;
  }


#menu__toggle {
  opacity: 0;
}
#menu__toggle:checked + .menu__btn > span {
  transform: rotate(45deg);
}
#menu__toggle:checked + .menu__btn > span::before {
  top: 0;
  transform: rotate(0deg);
}
#menu__toggle:checked + .menu__btn > span::after {
  top: 0;
  transform: rotate(90deg);
}
#menu__toggle:checked ~ .hamburger-menu{
  display: flex;
}
#menu__toggle:checked ~ .menu__box {
  left: 0 !important;
}
#menu__toggle:checked ~ .menu__btn{
  top: 40px;
  left: 50px;
  opacity: 1;
}
.menu__btnContene{
  width: 500px;
  display: flex;
  gap: 20px;
}
.menu__btn {
  position: fixed;
  top: 50px;
  left: 70px;
  width: 40px;
  height: 40px;
  cursor: pointer;
  z-index: 1;
  opacity: 0;
}
.menu__btn > span,
.menu__btn > span::before,
.menu__btn > span::after {
  display: block;
  position: absolute;
  width: 100%;
  height: 2px;
  background-color: #616161;
  transition-duration: .25s;
}
.menu__btn > span::before {
  content: '';
  top: -8px;
}
.menu__btn > span::after {
  content: '';
  top: 8px;
}
.menu__box {
  text-align: start;
  display: block;
  position: fixed;
  top: 0;
  left: -115%;
  width: calc(50% - 100px);
  height: 100%;
  margin: 0;
  padding: 145px 50px;
  list-style: none;
  border-radius: 0px 16px 16px 0px;
  background: #16141F;
  box-shadow: 0px 0px 35px 0px rgba(0, 0, 0, 0.15);
  transition-duration: .25s;
}
.menu__item {
  display: block;
  padding-bottom: 30px;
  color: #333;
  font-family: 'Roboto', sans-serif;
  font-size: 20px;
  font-weight: 600;
  text-decoration: none;
  transition-duration: .25s;
  color: var(--Grey-Light, #D0D0D0);
/* Menu */
  font-family: Golos;
  font-size: 14px;
  font-style: normal;
  font-weight: 500;
  line-height: normal;
  text-transform: uppercase;
}

.hamburger-menu{
  position: fixed;
  z-index: 9999;
  width: 100%;
}

.menu__btnContener{
  display: flex;
  align-items: center;
  width: 287px;
  justify-content: space-between;
}
.closeBatton{
  width: 48px;
  height: 48px;
  flex-shrink: 0;
  border-radius: 11px;
  background: #281941;
  display: flex;
  flex-direction: column;
  justify-content: center;
  color: var(--Grey-Light, #D0D0D0);
  text-align: center;
  font-family: "Font Awesome 6 Free";
  font-size: 20px;
  font-style: normal;
  font-weight: 900;
  line-height: normal;
}
}
@media only screen and (max-width: 743px) {
  .logOut{
    display: none;
  }
  .menu__btnContener{
    width: 100%;
    display: flex;
    justify-content: space-between;
    gap: 111px;
  }
  .menu__btnContener{
  display: flex;
  align-items: center;
  width: 305px;
  justify-content: space-between;
}
  .BannerContent{
    padding-top: 40px;
  }
  .logo{
    padding: 0 20px 28px;
    width: calc(100% - 40px);
    display: flex;
    justify-content: space-between;
  }
  .logoImg{
    width: 145px;
    height: 40px;
    flex-shrink: 0;
  }
  .dataContener{
    padding-top: 0;
  }
  .menu__box{
    left: -125%;
  }
  .menu__btn{
    left: 20px;
  }

#menu__toggle:checked ~ .logoImg img{
  width: 145px;
  height: 40px;
  flex-shrink: 0;
}
.menu__box {
  width: 100%;
}
.setCont{
  padding-top: 58px;
  display: flex;
  flex-direction: column;
  gap: 30px;
}
.setCont span{
  color: var(--Grey-Light, #D0D0D0);
/* Menu */
  font-family: Golos;
  font-size: 14px;
  font-style: normal;
  font-weight: 500;
  line-height: normal;
  text-transform: uppercase;
}
.lengSet{
  display: flex;
  gap: 15px;
  align-items: center;
}
}

</style>