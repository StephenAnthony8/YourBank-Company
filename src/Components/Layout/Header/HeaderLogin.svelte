<script>
  import { redirect } from "@sveltejs/kit";

</script>

<div class="header-login-signin flex">
  <a href="/signup" class="nav-link signup-button nav-padding">Sign Up</a>
  <a href="/login" class="nav-link login-button nav-padding">Login</a>
</div>

<style>
  .nav-link {
    border-radius: 82px;
  }

  .login-button {
    background-color: var(--clr-green-60);
    color: var(--clr-grey-11);
  }
  .header-login-signin {
    --gap: 30px;
  }

  @media (max-width: 1440px) {
    .header-login-signin {
      --gap: 20px;
    }
  }
</style>
