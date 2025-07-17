<script>
  import NavHeader from "./NavHeader.svelte";
  import HeaderLogo from "./HeaderLogo.svelte";
  import HeaderLogin from "./HeaderLogin.svelte";
  import "./Header.css";
  import { MediaQuery } from "svelte/reactivity";
  import MobileToast from "./MobileToast.svelte";
  
  const screenWidth = new MediaQuery("(min-width: 1050px)");
</script>

<header class="main-header flex">
  <!-- Logo -->
  <HeaderLogo />
  <!-- navigation bar -->
   {#if screenWidth.current}
   <NavHeader />
   <!-- Sign Up | Login | User -->
   <HeaderLogin />

  {:else}
  <!-- Dropdown menu icon (mobile) -->
   <MobileToast />
   {/if}
</header>

<style>
  .main-header {
    padding: 20px 34px;
    justify-content: space-between;
    align-items: center;
    border-radius: 100px;
    border: 1px solid var(--clr-grey-15);
    background: var(--clr-grey-11);
    font-size: var(--fs-18);
    margin: 0 var(--container-width-padding);

    @media (max-width: 1440px) {
      font-size: var(--fs-14);
    }
  }

</style>
