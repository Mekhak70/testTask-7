<div>
  <!-- Use the Banner component -->
  <Banner />
  <h1>This is the About Us page</h1>
</div>
</template>

<script lang="ts">
// Import the Banner component
import Banner from '../components/Banner.vue'; // Adjust the path based on your project structure

export default {
components: {
  // Register the Banner component
  Banner
}
};
</script>

<style>
/* Your styles for about.vue */
</style>