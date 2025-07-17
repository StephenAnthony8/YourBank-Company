<script>
  import FooterContact from "./FooterContact.svelte";

  import FooterExtras from "./FooterExtras.svelte";
  import FooterLogoNavigation from "./FooterLogoNavigation.svelte";
</script>

<footer class="Main-footer center flex">
  <!-- Logo (Plain Image) -->
  <FooterLogoNavigation />
  <div class="separator"></div>

  <!-- Contact info (Email, Phone, Location) -->
  <FooterContact />
  <div class="separator"></div>

  <!-- bottom bar : socials, copyright, privacy policy, Terms of service -->
  <FooterExtras />
</footer>

<style>
  footer {
    --gap: 50px;

    flex-direction: column;
  
    width: 100%;
    padding: 100px var(--container-width-padding) 50px;
    background-color: var(--clr-grey-11);

    @media (max-width: 1440px) {
      --gap: 40px;
      padding: 60px var(--container-width-padding) 30px;
    }
    @media (max-width: 1000px) {
      --gap: 30px;
      padding: 50px var(--container-width-padding) 30px;
    }
  }
</style>
