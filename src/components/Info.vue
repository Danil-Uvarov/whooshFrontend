<template>
  <section class="info-body">
    <h2 class="info__title">Express delivery market revolution</h2>
    <h4 class="info__subtitle">
      Express courier service in the city. We are a reliable logistics partner
      for delivery services for online stores and restaurants!
    </h4>
    <div class="info__row row">
      <div class="row__item item">
        <h5 class="item__title">Become a Courier</h5>
        <div class="item__images-courier">
          <img src="/image/item-courier.png" alt="" class="item__img" />
          <img src="/image/item-route.png" alt="" class="item__img-route" />
        </div>
        <p class="item__description">
          You choose a schedule. You decide how much and when to earn. Earnings
          from day one
        </p>
      </div>
      <div class="row__item item">
        <h5 class="item__title">Help & Support</h5>
        <img src="/image/item-support.png" alt="" class="item__img" />
        <p class="item__description">
          Door-to-door delivery in 90 minutes or at your convenience
        </p>
      </div>
      <div class="row__item item">
        <h5 class="item__title">Affiliate Program</h5>
        <img src="/image/item-affiliate.png" alt="" class="item__img" />
        <p class="item__description">
          Use our service and feel new quality of this traditional service!
        </p>
      </div>
    </div>
  </section>
</template>
<script setup lang="ts"></script>
<style scoped>
  .info-body {
    padding-bottom: 96px;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .info__title {
    font-family: 'Intro-bold';
    margin-top: 98px;
    font-weight: 700;
    font-size: 40px;
    line-height: 48px;
    text-align: center;
  }

  .info__subtitle {
    max-width: 754px;
    margin-top: 29px;
    font-weight: 400;
    font-size: 22px;
    line-height: 32px;
    text-align: center;
    color: rgba(29, 37, 60, 0.7);
  }

  .info__row {
    margin-top: 40px;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 50px;
  }

  .row__item {
    padding: 23px 24px 20px 24px;
    max-width: 300px;
    width: 100%;
    background-color: rgba(194, 210, 244, 0.2);
    border: 1px solid rgba(183, 198, 231, 1);
    border-radius: 8px;
  }

  .item__title {
    font-family: 'Intro-regular';
    font-weight: 400;
    font-size: 22px;
    line-height: 32px;
  }

  .item__images-courier {
    display: flex;
  }

  .item__img-route {
    margin-top: 17px;

    box-shadow: 16px;
  }

  .item__img {
    margin-top: 17px;
    max-width: 80px;
    max-height: 80px;
    border-radius: 100%;
    padding: 21px;
    background-color: #fff;
    box-shadow: 0px 12px 20px 3px rgba(43, 107, 243, 0.16);
  }

  .item__description {
    max-width: 250px;
    margin-top: 40px;
    font-weight: 400;
    font-size: 16px;
    text-align: left;
    color: rgba(102, 102, 102, 1);
  }

  @media (max-width: 1000px) {
    .info-body {
      padding-bottom: 48px;
      max-width: 328px;
      margin: 0 auto;
    }

    .info__title {
      margin: 54px 0px 0px 0px;
      font-size: 32px;
      line-height: 32px;
    }
    .info__subtitle {
      margin-top: 11px;
    }
    .info__description {
      margin: 11px 16px 0px 16px;
    }

    .info__row {
      margin-top: 15px;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      gap: 32px;
    }

    .item__images-courier {
      display: flex;
    }

    .item__img-route {
      margin-top: 17px;
      box-shadow: 16px;
    }
  }
</style>
