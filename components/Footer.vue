<template>
    <div class="footer">
        <div class="content-1">
            <div class="logo">
                <img :src="logoSrc" alt="Logo" />
            </div>
            <div class="text-container">
                <span>
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et
                    dolore magna aliqua.
                    Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
                    consequat.
                    Duis aute irure dolor in reprehenderit in.
                </span>
            </div>
            <div class="contact-icons-container">
                <img :src="facebookSrc" alt="Logo" />
                <img :src="twitterSrc" alt="Logo" />
                <img :src="instagramSrc" alt="Logo" />
            </div>
        </div>

        <div class="content-2">
            <div class="menu-items-container">
                <div class="menu-headline">
                    главное Меню
                </div>
                <ul>
                    <li>рейтинги</li>
                    <li>сервисы</li>
                    <li>обмен</li>
                    <li>отзывы</li>
                    <li>FAQ</li>
                    <li>о нас</li>
                    <li>контакты</li>
                </ul>

            </div>

            <div class="contact-box">
                <div class="menu-headline">
                    Связаться с нами
                </div>

                <div class="email-line">
                    <div class="email">
                        <img :src="messageIconSrc" alt="Logo" />
                        <span>support@crypto-info.cc</span>
                    </div>
                    <span class="note">Служба поддержки проекта</span>

                </div>

                <div class="time-line">
                    <img :src="timeIconSrc" alt="Logo" />
                    <span>Без выходных 09:00-20:00</span>
                </div>

                <div class="input-container">
                    <div class="input-wrapper">
                        <input />
                    </div>
                    <Button text="Подписаться" verticalPadding="13px" horizontalPadding="26px" fontSize="12px" />
                </div>

                <div class="privacy-content">
                    <span>
                        Все права защищены © 2024.
                        Любое копирование и воспроизведение текста, в том числе частичное и в любых формах,
                        без письменного разрешения правообладателя запрещено.
                    </span>

                </div>

            </div>
        </div>

    </div>
</template>
  
<script>

import Button from '@/components/common/Button.vue';

export default {
    components: {
        Button
    },
    data() {
        return {
            logoSrc: require('@/public/LOGO.svg'),
            ruFlagSrc: require('@/public/icons/ru.svg'),
            arrowSrc: require('@/public/icons/arrow.svg'),
            facebookSrc: require('@/public/contact-icons/facebook-icon.svg'),
            instagramSrc: require('@/public/contact-icons/instagram-icon.svg'),
            twitterSrc: require('@/public/contact-icons/twitter-icon.svg'),
            messageIconSrc: require('@/public/icons/message-icon.svg'),
            timeIconSrc: require('@/public/icons/time-icon.svg'),
        };
    }
};
</script>
  
  
<style>
.footer {
    display: flex;
    gap: 174px;
    height: 420px;
    background: #16141F;
    padding: 0 323px;
}

.content-1 {
    display: flex;
    flex-direction: column;
    gap: 17px;
    width: max-content;
    margin-top: 57px;
}

.content-2 {
    display: flex;
    gap: 190px;
    margin-top: 124px;
}

.text-container {
    width: 320px;
}

.text-container span {
    color: #D0D0D0;
    font-family: 'Golos', sans-serif;
    font-size: 15px;
    font-style: normal;
    font-weight: 400;
    line-height: 22px;
}

.contact-icons-container {
    display: flex;
    gap: 30px;
    padding-top: 5px;
}

.menu-items-container {
    display: flex;
    flex-direction: column;
    gap: 25px;
}

.menu-items-container>ul {
    display: flex;
    flex-direction: column;
    gap: 10px;
}

.menu-headline {
    color: #FFF;
    font-family: 'Golos', sans-serif;
    font-size: 14px;
    font-style: normal;
    font-weight: 700;
    line-height: normal;
    text-transform: uppercase;
}

.menu-items-container>ul>li {
    list-style: none;
    color: #D0D0D0;
    font-family: 'Golos', sans-serif;
    font-size: 14px;
    font-style: normal;
    font-weight: 500;
    line-height: normal;
    text-transform: uppercase;
    cursor: pointer;
}

.contact-box {
    display: flex;
    flex-direction: column;
    width: 468px;
    height: max-content;
    gap: 18px;
}

.email-line {
    display: flex;
    gap: 40px;
}

.email {
    display: flex;
    align-items: center;
    gap: 10px;
}

.email span {
    color: #D0D0D0;
    font-family: 'Golos', sans-serif;
    font-size: 14px;
    font-style: normal;
    font-weight: 700;
    line-height: normal;
}

.note {
    color: #D0D0D0;
    font-family: 'Golos', sans-serif;
    font-size: 14px;
    font-style: normal;
    font-weight: 400;
    line-height: normal;
}

.time-line span {
    color: #D0D0D0;
    font-family: 'Golos', sans-serif;
    font-size: 14px;
    font-style: normal;
    font-weight: 700;
    line-height: normal;
}

.time-line {
    display: flex;
    gap: 10px;
}

.input-container {
    display: flex;
    gap: 8px;
}

.input-wrapper {
    display: flex;
    align-items: center;
    background: #FFF;
    border-radius: 8px;
    padding: 0 16px;
    width: 335px;
}

.input-wrapper input:focus {
    border: none;
    outline: none;
}

.input-wrapper input {
    border: none;
    width: 100%;
}

.privacy-content span {
    color: rgba(255, 255, 255, 0.30);
    font-family: 'Golos', sans-serif;
    font-size: 13px;
    font-style: normal;
    font-weight: 500;
    line-height: normal;
}
</style>