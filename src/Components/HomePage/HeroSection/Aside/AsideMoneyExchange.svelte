<script lang="ts">
  import iconKenya from "$lib/assets/Icons/flag-icons/Kenya-Icon.svg";
  import iconJapan from "$lib/assets/Icons/flag-icons/Japan-Icon.svg";

  const moneyExchangeList = [
    {
      name: "Kenya Flag",
      icon: iconKenya,
      initials: "KES",
      currencyName: "Kenyan Shilling",
      value: "1,000.00",
    },
    {
      name: "Japan Flag",
      icon: iconJapan,
      initials: "JPY",
      currencyName: "Japanese Yen",
      value: "1,137.50",
    },
  ];
</script>

<div class="hero-section-money-exchange flex">
  <!-- Heading -->
  <h4 class="money-exchange-heading">Money Exchange</h4>
  <div class="currency-exchange-container flex">
    {#each moneyExchangeList as { name, icon, initials, currencyName, value }}
      <!-- Countries & Currency exchange Rates -->
      <div class=" money-exchange-currency-type">
        <!-- Icon & Currency Label -->
        <div class="internal-container-currency flex">
          <span class="icon-initial-container flex">

            <img src={icon} alt={`${name} Icon`} class="icon-sizing" />
            <!-- Initials -->
            <span class="currency-initials">{initials}</span>
          </span>
          <!-- Full name -->
          <p class="currency-name">{currencyName}</p>
        </div>
        <!-- Value -->
        <div class="hero-section-currency-value internal-container-currency">
          <p>{value}</p>
        </div>
      </div>
    {/each}
  </div>

  <button type="submit" class="money-exchange-submit"> Exchange </button>
</div>

<style>
  .hero-section-money-exchange {
    --gap: 25px;

    flex-direction: column;
    align-self: stretch;
    line-height: 150%;
  }
  .money-exchange-heading {
    font-size: 17px;
    font-weight: 500;
    line-height: 150%;
  }
  .currency-exchange-container {
    --gap: 0px;
    border-radius: 10px;
    align-self: stretch;
    border: 1px solid var(--clr-grey-15);
  }
  .money-exchange-currency-type {
    flex: 1 0 0;
    background-color: var(--clr-grey-11);
  }
  .internal-container-currency {
    --gap: 9px;
    flex-direction: column;
    align-items: flex-start;
    justify-content: center;
    align-self: stretch;
    border: 1px solid var(--clr-grey-15);
    padding: 17px;
    font-size: 13px;
  }
  .currency-initials {
    font-size: 15px;
    font-weight: 400;
  }
  .currency-name {
    font-size: 13px;
    font-weight: 300;
    color: var(--clr-white-90);
  }
  .hero-section-currency-value {
    font-weight: 500;
    font-size: 17px;
    padding-top: 26px;
    padding-bottom: 26px;
  }

  .money-exchange-submit {
    padding: 14px 26px;
    border-radius: 71px;
    background-color: var(--clr-dark-green);
    font-weight: 500;
    color: var(--clr-green-65);
    line-height: 150%;
    border: none;
  }

</style>
