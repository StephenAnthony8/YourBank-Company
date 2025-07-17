<script lang="ts">
  import iconCheckings from "$lib/assets/Icons/Products/Checking-accounts.svg";
  import iconSavings from "$lib/assets/Icons/Products/Savings-account.svg";
  import iconLoans from "$lib/assets/Icons/Products/Loans-mortgages.svg";
  const productList: {
    id: number;
    name: string;
    icon: string;
    explanationText: string;
  }[] = [
    {
      id: 1,
      name: "Checkings Account",
      icon: iconCheckings,
      explanationText:
        "Enjoy easy and convenient access to your funds with our range of checking account options. Benefit from features such as online and mobile banking, debit cards, and free ATM access.",
    },
    {
      id: 2,
      name: "Savings Account",
      icon: iconSavings,
      explanationText:
        "Build your savings with our competitive interest rates and flexible savings account options. Whether you're saving for a specific goal or want to grow your wealth over time, we have the right account for you.",
    },
    {
      id: 3,
      name: "Loans and Mortgages",
      icon: iconLoans,
      explanationText:
        "Realize your dreams with our flexible loan and mortgage options. From personal loans to home mortgages, our experienced loan officers are here to guide you through the application process and help you secure the funds you need.",
    },
  ];
</script>

<section class="products container flex">
  <!-- Products Heading & Description -->
  <div class="products-overview flex">
    <div class="products-overview-general flex">
      <h3 class="products-heading">
        Our <span class="green-text">Products</span>
      </h3>
      <p class="products-explanation">
        Discover a range of comprehensive and customizable banking products at
        YourBank, designed to suit your unique financial needs and aspirations
      </p>
    </div>
    <div class="products-option-tab rounded-container flex">
      <div class="individuals rounded-container flex">
        <p>For Individuals</p>
      </div>
      <div class="businesses rounded-container flex">
        <p>For Businesses</p>
      </div>
    </div>
  </div>

  <!-- Products List -->
  <ul class="products-list flex">
    {#each productList as { id, name, icon, explanationText }}
      <li class="products-container flex">
        <!-- Product Icon -->
        <div class="products-icon-container icon-container">
          <div class="products-icon-outer">
            <img
              src={icon}
              alt={`${name} icon`}
              class="products-icon icon-sizing"
            />
          </div>
        </div>
        <!-- Product Name and Explanation -->
         <div class="prodcuct-list-text">

           <h4 class="products-name">
             {name}
            </h4>
            <p class="products-explanation">
              {explanationText}
            </p>
          </div>
      </li>
      {#if id !== productList.length}
        <li class="products-list-separator separator-line"></li>
      {/if}
    {/each}
  </ul>
</section>

<style>
  .products {
    --gap: 80px;
    flex-direction: column;
    line-height: 150%;
  }
  .products-overview {
    --gap: 150px;
    justify-content: space-between;
    text-align: justify;
    align-items: flex-end;
  }
  .products-overview-general {
    --gap: 10px;
    flex-direction: column;
    align-self: stretch;
  }
  .products-heading {
    font-size: var(--fs-38);
    line-height: 150%;
    font-weight: var(--font-weight-500);
  }
  .products-explanation {
    font-size: var(--fs-16);
    line-height: 150%;
    color: var(--clr-grey-70);
    font-weight: var(--font-weight-300);
  }
  .products-option-tab {
    --gap: 0px;

    --padding-round-container-desktop: 12px;
    --padding-round-container-tablet: 10px;
    --padding-round-container-mobile: 8px;

    --border-round-container-radius-desktop: 82px;
    --border-round-container-radius-tablet: 15px;
    --border-round-container-radius-mobile: 10px;

    --bg-color: var(--clr-grey-11);

    border: 1px solid var(--clr-grey-15);
  }

  .individuals,
  .businesses {
    --padding-round-container-desktop: 10px 18px;
    --padding-round-container-tablet: 15px;
    --padding-round-container-mobile: 10px;

    --border-round-container-radius-desktop: 140px;
    --border-round-container-radius-tablet: 15px;
    --border-round-container-radius-mobile: 10px;

    margin: 0px;
    font-size: var(--fs-14);
    font-weight: var(--font-weight-400);
    text-wrap: nowrap;
  }
  .individuals {
    color: var(--clr-grey-11);
    --bg-color: var(--clr-green-60);
  }
  .products-list {
    --gap: 40px;
  }
  .products-container {
    --gap: 24px;
    flex-direction: column;
    align-items: center;
    text-align: center;
    padding-bottom: 24px;
  }
  .products-list-separator {
    --separator-line-color: var(--clr-dark-green);
    width: 5px;
  }
  .products-icon-container {
    --icon-size: fit-content;
    --icon-size-mobile: fit-content;
    border-radius: 70px;
    background: linear-gradient(
      180deg,
      rgba(202, 255, 51, 0.05) 0%,
      rgba(202, 255, 51, 0) 100%
    );
  }
  .products-icon-outer {
    padding: 14px;
    border-radius: 50px;
    background: linear-gradient(
      180deg,
      rgba(202, 255, 51, 0.1) -66.22%,
      rgba(202, 255, 51, 0) 85.46%
    );
  }
  .products-icon {
    --icon-size: 26px;
    --icon-size-mobile: 24px;
    object-fit: contain;
  }
  .products-name {
    font-size: var(--fs-20);
    line-height: 150%;
    font-weight: var(--font-weight-400);
    padding-bottom: 16px;
  }

  .products-explanation {
    font-size: var(--fs-16);
    color: var(--clr-grey-70);
    font-weight: var(--font-weight-300);
  }
</style>
