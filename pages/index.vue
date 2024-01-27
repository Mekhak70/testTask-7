<template>
  <div>
    <Banner />
    <CardsSection />
  </div>
</template>

<script>
// Import both components. Adjust paths as necessary.
import Banner from '@/components/banner.vue';
import SectionOne from '@/components/SectionOne.vue';
import CardsSection from '@/components/CardsSection.vue';

export default {
  name: 'IndexPage',
  components: {
    // Register both components for use in the template
    Banner,
    SectionOne,
    CardsSection
  }
}
</script>

<style>

</style>