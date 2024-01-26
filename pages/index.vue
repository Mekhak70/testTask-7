<template>
  <div>
    <Banner />
    <SectionOne />
  </div>
</template>

<script>
// Import both components. Adjust paths as necessary.
import Banner from '@/components/banner.vue';
import SectionOne from '@/components/SectionOne.vue';

export default {
  name: 'IndexPage',
  components: {
    // Register both components for use in the template
    Banner,
    SectionOne
  }
}
</script>

<style>
/* Styles for index.vue */
</style>