<template>
  <div class="card">
    <div class="card-image-info-wrapper">
      <div class="card-image">
        <img :src="imageSrc" alt="Card Image">
      </div>
      <div class="date_info">
        <div class="info_text">{{ date }}</div>
        <div class="views">
          <div class="view-number-wrapper">
            <img :src="eyeIconSrc" alt="Card Image">
            <div class="view-number">{{ viewNumber }}</div>
          </div>
          <div class="info_text">
            <img :src="publicIconSrc" alt="Card Image">
          </div>
        </div>

      </div>
    </div>

    <div class="card-texts-wrapper">
      <div class="card-text-headline">
        {{ title }}
      </div>
      <div class="card-text-content">
        {{ content }}
      </div>
      <div class="card-text-footer">
        <div class="visit-icon-wrapper">
          <img :src="visitIconSrc" alt="Card Image">
        </div>

        <div class="links-container">
          <div class="link">Безопасность</div>
          <div class="link">Проверенные сервисы</div>
          <div class="link">Интересное</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: String,
    content: String,
    imageSrc: String,
    date: String,
    viewNumber: String
  },
  data() {
    return {
      visitIconSrc: require('@/public/icons/visit-icon.svg'),
      eyeIconSrc: require('@/public/icons/eye-icon.svg'),
      publicIconSrc: require('@/public/icons/back-icon.svg'),
    };
  }
}
</script>

<style scoped>
.card {
  background: #171520;
  padding: 20px;
  border-radius: 16px;
  overflow: hidden;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  display: flex;
  max-width: 865px;
  gap: 10px;
}

.card-image img {
  width: 100%;
  max-width: 340px;
  height: auto;
  display: block;
}

.card-content {
  padding: 16px;
}

.card-footer {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 16px;
  border-top: 1px solid #eeeeee;
}

.date_info {
  display: flex;
  justify-content: space-between;
  padding: 5px 6px;
  background: rgba(255, 255, 255, 0.02);
  border-radius: 10px;
}

.info_text {
  color: #D0D0D0;
  font-family: 'Golos', sans-serif;
  font-size: 14px;
  font-style: normal;
  font-weight: 500;
  line-height: normal;
  padding: 8px;
}

.card-image-info-wrapper {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.card-texts-wrapper {
  display: flex;
  flex-direction: column;
  width: auto;
  gap: 16px;
  max-width: 475px;
}

.views {
  display: flex;
  padding: 0 8px;
  gap: 5px;
  width: 135px;
}

.view-number-wrapper {
  display: flex;
  align-items: center;
  padding-right: 8px;
  gap: 6px;
}

.view-number {
  color: #D0D0D0;
  font-family: 'Golos', sans-serif;
  font-size: 14px;
  font-style: normal;
  font-weight: 500;
  line-height: normal;
}

.card-text-headline {
  color: #FFF;
  font-family: 'Golos', sans-serif;
  font-size: 18px;
  font-weight: 500;
  line-height: normal;
  text-wrap: wrap;
  padding: 5px 16px 0 6px;
}

.card-text-content {
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-line-clamp: 10;
  overflow: hidden;
  height: 203px;
  text-overflow: ellipsis;
  color: #D0D0D0;
  font-family: 'Golos', sans-serif;
  font-size: 14px;
  font-weight: 400;
  line-height: 20px;
  text-wrap: wrap;
  padding: 0px 16px 0 6px;
}

.card-text-footer {
  display: flex;
  align-items: flex-end;
  gap: 20px;
}

.links-container {
  display: flex;
  height: 16px;
  gap: 10px;
}

.visit-icon-wrapper {
  display: flex;
  align-items: flex-end;
  width: 18px;
}

.visit-icon-wrapper img {
  width: 18px;
  aspect-ratio: 1/1;
}

.link {
  color: #D0D0D0;
  font-family: 'Golos', sans-serif;
  font-size: 13px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
}
@media only screen and (max-width: 1167px) {
  .card-texts-wrapper {
  max-width: 100%;
}
  .card {

  max-width: 100%;

}
}
@media only screen and (max-width: 743px) {
  .neonmanContener{
    display: none;
  }
  .card{
    display: flex;
    width: 100%;
    padding:0;
    flex-direction: column;
    align-items: flex-start;
    gap: 10px;
  }
  .cards-section{
    padding: 0;
  }
  .card-image img {
  max-width: 100% ;
  height: auto;
  display: block;
}

  .card-image-info-wrapper {
      width: 100%;
}
}


</style>