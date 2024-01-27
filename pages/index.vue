<template>
  <div>
    <Banner />
    <CardsSection />
    <Footer />
  </div>
</template>

<script>
// Import both components. Adjust paths as necessary.
import Banner from '@/components/banner.vue';
import CardsSection from '@/components/CardsSection.vue';
import Footer from '@/components/Footer.vue';

export default {
  name: 'IndexPage',
  components: {
    Banner,
    CardsSection,
    Footer
  }
}
</script>

<style>

</style>