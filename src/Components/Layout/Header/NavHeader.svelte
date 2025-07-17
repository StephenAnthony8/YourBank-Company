<script lang="ts">
  import { page } from "$app/state";
  const currentPath: string = $derived(page.url.pathname);
  const routes: Array<{ path: string; label: string }> = [
    { path: "/", label: "Home" },
    { path: "/careers", label: "Careers" },
    { path: "/about", label: "About" },
    { path: "/security", label: "Security" },
  ];
</script>

<nav class="nav-header flex">
  {#each routes as route}
    <a
      href={route.path}
      class={`${currentPath === route.path ? "active" : ""} nav-padding`}
    >
      {route.label}
    </a>
  {/each}
</nav>

<style>
  .nav-header {
    --gap: 26px;
    justify-content: space-between;
    align-items: center;
    max-width: fit-content;
  }

  .active {
    border-radius: 82px;
    background-color: var(--clr-grey-15);
  }

  @media (max-width: 1440px) {
  }
  @media (max-width: 1000px) {
  }

  /* To be done once I find an appropriate design */
  @media (max-width: 600px) {
  }
</style>
