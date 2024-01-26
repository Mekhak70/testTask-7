<template>
  <div class="banner">
    <div class="BannerContent">
      <HeaderComp/>
      <BannerContent/>
    </div>


  </div>
</template>

<script>
// Import both components. Adjust paths as necessary.
import HeaderComp from '@/components/header.vue';
 import BannerContent from '@/components/BannerContent.vue';


export default {
  name: 'HeaderPage',
  components: {
    // Register both components for use in the template
    HeaderComp,
    BannerContent

  }
}
</script>

<style>
.banner {
  width: 100%;
  height: 800px;
  background-color: black; /* Teal background */
  color: white; /* White text */
  text-align: center; /* Centered text */
}
.BannerContent{
  padding-top: 70px;
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>