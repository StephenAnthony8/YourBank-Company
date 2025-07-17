<script lang="ts">
  import HeroSectionAside from "./Aside/HeroSectionAside.svelte";
  import HeroSectionMain from "./Main/HeroSectionMain.svelte";
</script>

<section class="hero-section flex">
  <!-- Hero Section
  Contains:
  
  section 2
  - Demo operations section
  - Supported currency section
  - Abstract vector design
  -->
  <HeroSectionMain />
  <HeroSectionAside />
</section>

<style>
  .hero-section {
    --gap: 120px;
    padding: 100px 0px;

    @media (max-width: 1440px) {
      --gap: 100px;
      padding: 60px 0px;
    }
    @media (max-width: 1050px) {
      flex-direction: column;
      justify-content: center;
      align-items: center;
      padding: 40px 0px;
    }

    @media (max-width: 600px) {
      --gap: 80px;
      padding: 16px;
    }
  }
</style>
