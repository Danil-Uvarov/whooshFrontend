<template>
  <section class="intro__body">
    <img src="/image/intro-city.png" alt="" class="intro__bacground-img-city" />
    <h2 class="intro__title">What we do</h2>
    <h4 class="intro__subtitle">
      Express courier service in the city. We are a reliable logistics partner
      for delivery services for online stores and restaurants!
    </h4>
    <div class="intro__row">
      <div class="intro__item item">
        <div class="item__image-wrapper">
          <img src="/image/intro-calculation.png" alt="" class="item__image" />
        </div>
        <h5 class="item__title">
          Online <a href="" class="item__title-link">calculation</a>
        </h5>
        <p class="item__subtitle">
          Instant calculation of the cost in the order form, the price is
          updated in the process of filling out the form
        </p>
      </div>
      <div class="intro__item item">
        <div class="item__image-wrapper">
          <img src="/image/intro-proverki.png" alt="" class="item__image" />
        </div>
        <h5 class="item__title">Minimum paperwork</h5>
        <p class="item__subtitle">
          You can place an order for courier or freight delivery without
          registration and contract.
        </p>
      </div>
      <div class="intro__item item">
        <div class="item__image-wrapper">
          <img src="/image/intro-payment.png" alt="" class="item__image" />
        </div>
        <h5 class="item__title">Convenient payment</h5>
        <p class="item__subtitle">
          You can pay for delivery by card or in cash at any of the order
          addresses. For legal entities non-cash is available.
        </p>
      </div>
    </div>
    <button class="intro__button-yellow">Get started!</button>
  </section>
</template>
<script setup lang="ts"></script>
<style scoped>
  .intro__body {
    position: relative;
    padding-bottom: 72px;
    background-color: #f1f4fc;
    border-radius: 400px 0px 0px 400px;
    left: -2%;
    width: 102%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

  .intro__bacground-img-city {
    position: absolute;
    top: -80px;
    right: 0px;
    z-index: 2;
  }

  .intro__title {
    margin-top: 74px;
    font-weight: 700;
    font-size: 40px;
    line-height: 48px;
    text-align: center;
  }

  .intro__subtitle {
    margin-top: 29px;
    max-width: 754px;
    text-align: center;
    font-weight: 400;
    font-size: 22px;
    line-height: 32px;
    color: rgba(29, 37, 60, 0.5);
  }

  .intro__row {
    margin-top: 39px;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 50px;
  }

  .intro__item {
    max-width: 300px;
  }

  .item__image-wrapper {
    width: 100%;
    height: 100%;
    max-width: 38px;
    max-height: 38px;
    padding: 32px;
    background-color: #fff;
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .item__image {
    width: 38px;
    height: 38px;
  }

  .item__title {
    margin-top: 31px;
    font-weight: 400;
    font-size: 22px;
    line-height: 32px;
  }

  .item__title-link {
    font-weight: 400;
    font-size: 22px;
    line-height: 32px;
    color: rgba(43, 107, 243, 1);
  }

  .item__subtitle {
    margin-top: 20px;
    font-weight: 400;
    font-size: 16px;
    color: rgba(102, 102, 102, 1);
  }

  .intro__button-yellow {
    width: 100%;
    max-width: 298px;
    margin-top: 36px;
    padding: 16px 96px;
    background-color: rgba(255, 221, 45, 1);
    border-radius: 32px;
    border: none;
    font-weight: 400;
    font-size: 18px;
    line-height: 32px;
    align-items: center;
    white-space: nowrap;
  }

  @media (max-width: 1100px) {
    .intro__body {
      border-radius: 0;
      padding: 0 16px 48px 16px;
    }
    .intro__title {
      margin-top: 54px;
    }
    .intro__subtitle {
      margin-top: 11px;
    }
    .intro__row {
      flex-direction: column;
      align-items: center;
      margin-top: 31px;
    }
    .intro__item {
      display: flex;
      flex-direction: column;
      align-items: center;
    }
    .item__subtitle {
      text-align: center;
    }
    .intro__bacground-img-city {
      display: none;
    }
  }
</style>
