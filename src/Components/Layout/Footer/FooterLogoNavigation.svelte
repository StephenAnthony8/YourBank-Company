<script>
  import footerLogo from "$lib/assets/Logo/Logo-Desktop.svg";
</script>

<div class="footer-logo-navigation center flex">
  <div class="footer-logo">
    <img src={footerLogo} alt="YourBank Logo" />
  </div>
  <!-- Navbar (unhighlighted) -->
  <nav class="footer-nav flex">
    <a href="/">Home</a>
    <a href="/careers">Careers</a>
    <a href="/about">About</a>
    <a href="/security">Security</a>
  </nav>
</div>

<style>
  .footer-logo-navigation {
    --gap: 50px;
    flex-direction: column;
    width: 100%;

    @media (max-width: 1440px) {
      --gap: 40px;
    }
    @media (max-width: 1000px) {
      --gap: 24px;
    }
  }

  .footer-nav {
    --gap: 26px;

    @media (max-width: 1440px) {
      --gap: 14px;
    }
    @media (max-width: 1000px) {

  }
  }
</style>
