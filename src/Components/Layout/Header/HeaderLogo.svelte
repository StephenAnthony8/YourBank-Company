<script lang="ts">
  import logoDesktop from "$lib/assets/Logo/Logo-Desktop.svg";
  import logoMobile from "$lib/assets/Logo/Logo-Mobile.svg";
  import logoLaptop from "$lib/assets/Logo/Logo-Laptop.svg";
  import { MediaQuery } from "svelte/reactivity";

  const isMobile = new MediaQuery("(max-width: 600px)");
  const isLaptop = new MediaQuery("(max-width: 1440px) and (min-width: 451px)");
  const isDesktop = new MediaQuery("(min-width: 1441px)");
  let logoImage: string = $derived(
    isDesktop.current ? logoDesktop : isLaptop.current ? logoLaptop : logoMobile
  );
</script>

<div class="nav-logo">
  <a href="/">
    <img src={logoImage} alt="YourBank Logo" class="logo-image" />
  </a>
</div>

<style>
</style>
