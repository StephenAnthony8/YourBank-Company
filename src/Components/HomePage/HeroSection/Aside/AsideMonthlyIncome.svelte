<div class="hero-section-monthly-income flex">
  <!-- Monthly income icon -->
  <div class="icon-container green-60 circle flex center">
    <svg
      viewBox="0 0 22 21"
      fill="none"
      xmlns="http://www.w3.org/2000/svg"
      class="icon-sizing"
    >
      <path
        fill-rule="evenodd"
        clip-rule="evenodd"
        d="M10.7036 4.60156C11.0627 4.60156 11.3538 4.8927 11.3538 5.25184V9.80378H15.9058C16.2649 9.80378 16.5561 10.0949 16.5561 10.4541C16.5561 10.8132 16.2649 11.1043 15.9058 11.1043H11.3538V15.6563C11.3538 16.0154 11.0627 16.3066 10.7036 16.3066C10.3444 16.3066 10.0533 16.0154 10.0533 15.6563V11.1043H5.50135C5.14221 11.1043 4.85107 10.8132 4.85107 10.4541C4.85107 10.0949 5.14221 9.80378 5.50135 9.80378L10.0533 9.80378V5.25184C10.0533 4.8927 10.3444 4.60156 10.7036 4.60156Z"
        fill="#1A1A1A"
      />
    </svg>
  </div>
  <span class="income-context">

    <p class="income-context-amount">+ $5,000.00</p>
    <p class="income-context-label">Monthly Income</p>
  </span>
</div>

<style>
  .hero-section-monthly-income {
    --gap: 9px;

    padding: 14px 17px;
    border-radius: 10px;
    background-color: var(--clr-dark-green);
    width: fit-content;
    flex-shrink: 0;

    position: absolute;
    top: -43px;
    left: -61px;
  }
  .hero-section-monthly-income p{
    line-height: 150%;
  }
  .income-context-amount {
    font-size: 17px;
    font-weight: 400;

  }
  .income-context-label {
    font-size: 13px;
    font-weight: 300;
    color: var(--clr-white-90);
  }
</style>
