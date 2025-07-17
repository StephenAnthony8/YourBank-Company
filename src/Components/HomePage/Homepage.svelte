<script lang="ts">
import HeroSection from './HeroSection/HeroSection.svelte';
  import Products from './Products/Products.svelte';
</script>
<section class="homepage subsection-container flex">
  <HeroSection />
  <Products />

</section>

<style>
  .homepage {
    flex-direction: column;
  }
    
</style>
