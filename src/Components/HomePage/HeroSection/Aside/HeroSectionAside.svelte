<script lang="ts">
  import type { Component } from "svelte";

  import AsideTransaction from "./AsideTransaction.svelte";
  import AsideMoneyExchange from "./AsideMoneyExchange.svelte";
  import AsideMonthlyIncome from "./AsideMonthlyIncome.svelte";
  import AsideCurrency from "./AsideCurrency.svelte";
  import AsideVector from "./AsideVector.svelte";
</script>

<!-- To do: add  a background& vector image -->

<aside class="hero-section-aside flex">
  <!-- Monthly income section -->
  <AsideMonthlyIncome />
  <!-- Transactions section -->
  <AsideTransaction />
  <!-- Money exchange section -->
  <AsideMoneyExchange />

  <!-- Supported currency section -->
  <AsideCurrency />
  <!-- Abstract vector design -->

  <AsideVector />
</aside>

<style>
  .hero-section-aside {
    position: relative;
    line-height: 150%;
    flex-shrink: 0;
    flex-direction: column;
    border: 1px solid var(--clr-grey-15);

    /* Implement glassy green reflect border at the top right corner and bottom left corner */

    

    --gap: 26px;
    border-radius: 18px;
    width: 515px;
    padding: 34px;

    @media (max-width: 1400px) {
      --gap: 21px;
      width: 410px;
      padding: 27px;
      border-radius: 8px;
    }
    @media (max-width: 600px) {
      --gap: 15px;
      width: 305px;
      padding: 20px;
      border-radius: 6px;
    }
  }
  .hero-section-aside::after {
    content: "";
    position: absolute;
    top: 0;
    right: 0;
    width: calc(100% + 1px);
    height: calc(100% + 1px);
    background-color: var(--clr-aside-dark);
    border-radius: 18px;
    z-index: -1;
  }
</style>
