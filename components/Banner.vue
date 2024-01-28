<template>
  <div class="banner">
    <div class="BannerContent">
      <HeaderComp />
      <BannerContent />
    </div>


  </div>
</template>

<script>

import HeaderComp from '@/components/Header.vue';
import BannerContent from '@/components/BannerContent.vue';


export default {
  name: 'HeaderPage',
  components: {
    HeaderComp,
    BannerContent

  },

  data() {
    return {
      coverSrc: require('@/public/banner-cover/cover.jpg'),

    };
  }


}


// Other component options go here
</script>

<style>
.banner {
  width: 100%;
  height: 800px;
  color: white;
  /* White text */
  text-align: center;
  /* Centered text */
  background-image: url('@/public/banner-cover/cover.jpg');

  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
}

.BannerContent {
  padding-top: 70px;
  display: flex;
  flex-direction: column;
  align-items: center;
}

@media only screen and (max-width: 1167px) {
  .BannerContent {
    width: 100%;
    padding: 44px 0 0;
  }

  .banner {
    height: 1065px;
  }
}

@media only screen and (max-width: 743px) {
  .banner {
    height: 845px;
  }
}</style>