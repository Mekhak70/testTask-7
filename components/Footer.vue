<template>
    <div class="footer">
        <div class="content-1">
        <div class="contentSmall">
            <div class="logoFooter">
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
        </div>
            <div class="content-2">

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
                        <input type="text"/>
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
    min-height: 420px;
    background: #16141F;
    padding: 0 323px;
}

.content-1 {
    display: flex;

    gap: 174px;
    width: max-content;

}
.menu-items-container{
     padding-top: 124px;
}
.contentSmall{
    display: flex;
    flex-direction: column;
    gap: 17px;
    width: max-content;
    padding-top: 57px;
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
@media only screen and (max-width: 744px) {
    .logoFooter{
        padding-left: 0;
    }
    .footer{
        display: flex;
        flex-direction: column;
        padding: 60px 41px 40px 41px;
        flex-direction: column;

        gap: 50px;

    }
    .content-1{
        display: flex;
        width: 604px;
        /* align-items: flex-end; */
        gap: 80px;
        padding-left: 28px;
    }
    .content-2{
        justify-content: start;
        padding-left: 28px;
        margin-top: 0;
    }
    .contentSmall{
        padding-top: 0;
    }
    .menu-items-container{
        padding-top: 65px;
    }
}
@media only screen and (max-width: 390px) {
    .text-container{
        display: none;
    }
    .contentSmall{
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
        height: 48px;
        gap: 64px;
    }
    .footer{
        display: flex;
        padding: 60px 20px 40px 20px;
        flex-direction: column;
        align-items: center;
        gap: 50px;
    }
    .content-1{
        width: 350px;
        display: flex;
        flex-direction: column;
        padding-left: 0;
        gap: 40px;
    }
    .input-container{
        display: flex;
        flex-direction: column;
        gap: 15px;
    }
    .contact-icons-container{
        padding-top: 0;
        gap: 10px;
    }
    .contact-icons-container img{
        width: 30.625px;
        height: 35px;
    }
    .logoFooter img{
        width: 173.693px;
        height: 44.764px;
        flex-shrink: 0;
    }
    .menu-items-container {
    padding-top: 0;
}
.menu-headline{
    padding-bottom: 6px;
    color: var(--White, #FFF);
    font-family: Golos;
    font-size: 14px;
    font-style: normal;
    font-weight: 700;
    line-height: normal;
    text-transform: uppercase;
}
.menu-headline ul li{
    color: var(--Grey-Light, #D0D0D0);
    /* Menu */
    font-family: Golos;
    font-size: 14px;
    font-style: normal;
    font-weight: 500;
    line-height: normal;
    text-transform: uppercase;

}
.contact-box{
    display: flex;
    width: 350px;
    flex-direction: column;

}
.input-wrapper{
    width: 316px;
    height: 6px;
    display: flex;
    padding: 17px 16px;
    align-items: center;
    gap: 10px;
    align-self: stretch;
}
.email-line{
    display: flex;
    flex-direction: column;
}
.note{
    display: none;
}
.content-2{
    padding-left: 0;
}
.time-line{
    align-items: center;
}
}
</style>