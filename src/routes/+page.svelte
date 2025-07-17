<!-- Home Page -->
<script lang="ts">
  import { setContext } from "svelte";
  import Homepage from "../Components/HomePage/Homepage.svelte";
  import "../index.css";
  import { MediaQuery } from "svelte/reactivity";

  // Media Queries: Screen resolutions
  const isDesktop: MediaQuery = new MediaQuery("(min-width: 1441px)");
  const isLaptop: MediaQuery = new MediaQuery(
    "(min-width: 1051px) and (max-width: 1440px)"
  );
  const isTablet: MediaQuery = new MediaQuery(
    "(min-width: 601px) and (max-width: 1050px)"
  );
  const isMobile: MediaQuery = new MediaQuery("(max-width: 600px)");

  setContext("mediaQueries", { isDesktop, isLaptop, isTablet, isMobile });
</script>

<Homepage />
