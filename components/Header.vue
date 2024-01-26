<template>
    <div class="header">
     <div class="logo">
        <img :src="logoSrc" alt="Logo" />
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
            <span>войти</span>
            </div>
            <div class="flag">
                <img :src="ruFlagSrc" alt="RU flag" />
                <img :src="arrowSrc" alt="Arrow icon"/>
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
      ruFlagSrc:require('@/public/ru.svg'),
      arrowSrc:require('@/public/arrow.svg')
    };
  }
  // Other component options go here
};
</script>


  <style>
  *{
    padding: 0;
    margin: 0;
  }
  .header {
    width: 66.354%;
    height: 40px;
    display: flex;
    justify-content: space-between;
    background-color: black; /* Teal background */
    color: white; /* White text *//* Some padding */

  }
  .logo{
    display: flex;
    width: 145px;
    height: 40px;
    padding: 1.667px 0.256px 1.03px 0px;
    justify-content: center;
    align-items: center;
    flex-shrink: 0;
  }
  .menu{
    display: flex;
    align-items: center;
    gap: 80px;
  }
  .menu > ul{
    display: flex;
    gap: 30px;
  }
  .menu > ul > li {
    list-style: none;
    color: var(--Grey-Light, #D0D0D0);
/* Menu */
    font-family: Golos;
    font-size: 14px;
    font-style: normal;
    font-weight: 500;
    line-height: normal;
    text-transform: uppercase;

  }
  .logOut{
    display: flex;
    align-items: center;
    gap: 15px;
  }
  .flag{
    display: flex;
    padding: 12px;
    justify-content: center;
    align-items: center;
    gap: 8px;
    border-radius: 11px;
    background: rgba(255, 255, 255, 0.10);
  }
  .flag span{
    color: var(--Grey-Light, #D0D0D0);
    font-family: "Font Awesome 6 Free";
    font-size: 12px;
    font-style: normal;
    font-weight: 900;
    line-height: 15px; /* 125% */
    text-transform: uppercase;
  }

  </style>