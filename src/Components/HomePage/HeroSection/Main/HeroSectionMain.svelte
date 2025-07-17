<script lang="ts">
</script>

<section class="hero-section-main flex">
  <!-- Promotional text -->
  <div class="hero-section-text flex">
    <div class="hero-section-promotional-text flex">
      <!-- Promotional text checkmark icon : svg-->
      <svg
        viewBox="0 0 24 24"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
        class="icon-sizing"
      >
        <path
          fill-rule="evenodd"
          clip-rule="evenodd"
          d="M8.60288 3.79876C9.42705 2.85093 10.6433 2.25 12 2.25C13.3566 2.25 14.5728 2.85087 15.397 3.79861C16.6501 3.71106 17.9352 4.14616 18.8946 5.10557C19.854 6.06498 20.2891 7.35009 20.2016 8.60319C21.1492 9.42735 21.75 10.6435 21.75 12C21.75 13.3568 21.149 14.5731 20.2011 15.3973C20.2884 16.6502 19.8533 17.935 18.8941 18.8943C17.9348 19.8535 16.65 20.2886 15.3971 20.2013C14.5729 21.1491 13.3567 21.75 12 21.75C10.6434 21.75 9.4272 21.1491 8.60304 20.2014C7.34992 20.289 6.0648 19.8539 5.10537 18.8945C4.14596 17.935 3.71086 16.6499 3.79841 15.3968C2.85079 14.5726 2.25 13.3565 2.25 12C2.25 10.6434 2.85085 9.42723 3.79855 8.60306C3.7111 7.35005 4.14621 6.06507 5.10554 5.10574C6.06488 4.1464 7.34987 3.71129 8.60288 3.79876ZM15.6103 10.1859C15.8511 9.84887 15.773 9.38046 15.4359 9.1397C15.0989 8.89894 14.6305 8.97701 14.3897 9.31407L11.1543 13.8436L9.53033 12.2197C9.23744 11.9268 8.76256 11.9268 8.46967 12.2197C8.17678 12.5126 8.17678 12.9874 8.46967 13.2803L10.7197 15.5303C10.8756 15.6862 11.0921 15.7656 11.3119 15.7474C11.5316 15.7293 11.7322 15.6153 11.8603 15.4359L15.6103 10.1859Z"
          fill="#CAFF33"
        />
      </svg>
      <p class="capitalize">No LLC Required, No Credit Check.</p>
    </div>
    <div class="main-text-area flex">
      <!-- Hero text heading -->
      <h2 class="hero-section-heading">
        Welcome to YourBank
        <p class="capitalize">
          Empowering your
          <span class="capitalize">Financial Journey</span>
        </p>
      </h2>
      <!-- Hero text explanation -->
      <p class="hero-section-explanation">
        At YourBank, our mission is to provide comprehensive banking solutions
        that empower individuals and businesses to achieve their financial
        goals. We are committed to delivering personalized and innovative services
        that prioritize our customers' needs.
      </p>
    </div>
  </div>
  <!-- Open account button  -->
  <button class="open-account"> Open Account </button>
</section>

<style>
  .hero-section-main {
    --gap: 50px;

    flex-direction: column;
    font-size: var(--fs-18);
    line-height: 150%;
    font-weight: var(--font-weight-300);
    max-width: 50%;

    @media (max-width: 1440px) {
      --gap: 40px;

      font-size: var(--fs-16);
    }
    @media (max-width: 1050px) {
      --gap: 30px;
      max-width: 100%;

      font-size: var(--fs-14);
    }
    @media (max-width: 600px) {
      font-size: var(--fs-12);
      text-align: center;
      justify-content: center;
      align-items: center;
    }
  }
  .hero-section-text {
    --gap: 20px;
    flex-direction: column;

    @media (max-width: 600px) {
      justify-content: center;
      align-items: center;
    }
  }
  .hero-section-promotional-text {
    --gap: 4px;
    align-items: center;

    padding: 10px 20px 10px 10px;
    border-radius: 61px;
    background-color: var(--clr-grey-15);
    max-width: fit-content;

    line-height: 24px;

    @media (max-width: 1440px) {
      --icon-size: 20px;

      padding: 8px 16px 8px 8px;
    }
  }
  .hero-section-promotional-text p {
    margin: auto;
  }
  .main-text-area {
    gap: 14px;
    flex-direction: column;
  }
  .hero-section-heading {
    font-size: var(--fs-48);

    font-weight: var(--font-weight-500);
    line-height: 150%;
    margin: 0;

    @media (max-width: 1440px) {
      font-size: var(--fs-38);
    }
    @media (max-width: 1050px) {
      font-size: var(--fs-28);
    }
  }
  .hero-section-heading p {
    margin: 0;
  }
  .hero-section-heading span {
    color: var(--clr-green-60);
  }
  .hero-section-explanation {
    color: var(--clr-white-90);
    margin: 0;
  }
  .open-account {
    padding: 18px 30px;
    border-radius: 82px;
    text-align: center;
    max-width: fit-content;
    background-color: var(--clr-green-60);
    border-color: transparent;
    font-weight: var(--font-weight-400);
    color: var(--clr-grey-11);

    @media (max-width: 1440px) {
      padding: 14px 24px;
    }
  }
  .open-account:hover {
    background-color: var(--clr-green-70);
  }
  .open-account:active {
    background-color: var(--clr-green-80);
  }
</style>
