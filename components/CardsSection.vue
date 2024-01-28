<template>
    <div class="cards-section">
        <div class="cards">
            <div class="cards-container">
                <CardComponent v-for="card in cards" :key="card.id" :title="card.title" :content="card.content"
                    :imageSrc="card.imageSrc" :date="card.date" :viewNumber="card.viewNumber" />
            </div>
            <div class="button-wrapper">
                <Button text="Больше новостей" />
            </div>
        </div>
        <div class="side-bar">
            <SideBarCardComponent v-for="card in sideCards" :key="card.id" :companyIconSrc="card.companyIconSrc"
                :companyName="card.companyName" :content="card.content" :image="card.image" :viewNumber="card.viewNumber"
                :date="card.date" />
        </div>
    </div>
</template>

<script>
// Import the CardComponent
import CardComponent from '@/components/common/CardComponent.vue';
import SideBarCardComponent from '@/components/common/SideBarCard.vue';
import Button from '@/components/common/Button.vue';
import { cardsData } from '@/static/data/cards-data.js';

export default {
    components: {
        CardComponent,
        SideBarCardComponent,
        Button
    },
    data() {
        return {
            cards: cardsData.cards,
            sideCards: cardsData.sideCards,
        }
    }
}
</script>

<style scoped>
.cards-section {
    display: flex;
    gap: 49px;
    padding: 80px 323px;
    background: radial-gradient(50.31% 45.06% at 10.16% 91.73%, rgba(251, 21, 96, 0.08) 0%, rgba(0, 0, 0, 0.00) 100%), radial-gradient(59.34% 35.83% at 93.49% 46.73%, rgba(111, 17, 237, 0.20) 25.5%, rgba(0, 0, 0, 0.00) 100%), linear-gradient(98deg, #16141F 19.74%, #100F16 100%);
    scrollbar-width: none;
}

.cards-section::-webkit-scrollbar {
    display: none;
    width: 0;
}

.cards-container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    gap: 30px;
}
.side-bar {
    display: flex;
    flex-direction: column;
    gap: 20px;
    width: 320px;
    background: #171520;
    border-radius: 14px;
    box-shadow: 0px 0px 35px 0px rgba(0, 0, 0, 0.15);
    padding: 20px;
}

.cards {
    display: flex;
    flex-direction: column;
    gap: 30px;
}

.button-wrapper{
    display: flex;
    align-items: center;
    justify-content: center;
}
@media only screen and (max-width: 744px) {
  /* Hide the menu on screens with a maximum width of 744px */
  .cards-section {
    padding: 60px 50px ;
    flex-direction: column;
  }
  .side-bar{
        display: none;
    }

}
@media only screen and (max-width: 390px) {
  /* Hide the menu on screens with a maximum width of 744px */
  .cards-section {
    padding:0;
  }
  .button-wrapper{
    padding-bottom: 40px;
  }
}
</style>