<template>
  <section class="main-body">
    <div class="main__left-block">
      <div class="main__info info">
        <h2 class="info__title">Our service started work in New York</h2>
        <p class="info__text">
          We make delivery exactly at the time you need - we can start to
          fulfill the order a few minutes after it arrives, or we can deliver on
          a specific day and hour.
        </p>
        <button class="info__button">
          Read more
          <img src="/image/info-button.png" alt="" class="info__button-image" />
        </button>
      </div>
      <div class="main__video-block video">
        <h3 class="video__title">How it works</h3>
        <img src="/image/Video.png" alt="" class="video-img" />
        <div class="video__pagging pagging">
          <img
            src="/image/video-pagging-blue.png"
            alt=""
            class="pagging__img-active"
          />
          <img src="/image/video-pagging.png" alt="" class="pagging__img" />
          <img src="/image/video-pagging.png" alt="" class="pagging__img" />
          <img src="/image/video-pagging.png" alt="" class="pagging__img" />
        </div>
      </div>
    </div>
    <div class="main__right-block">
      <OrderForm class="order-form" />
      <div class="main__tracking tracking">
        <h3 class="tracking__title">Track a package</h3>
        <div class="tracking__input-wrapper">
          <input type="text" placeholder="Enter code" class="tracking-input" />
          <img
            src="/image/tracking-loupe.png"
            alt=""
            class="tracking__loupe-img"
          />
        </div>
      </div>
    </div>
  </section>
</template>
<script setup lang="ts">
  import OrderForm from './main/OrderForm.vue'
</script>
<style scoped>
  .main-body {
    background-repeat: no-repeat;
    background: url('/image/main-bacground.png') no-repeat center bottom;
    background-color: #f1f4fc;
    padding: 66px 32px 32px 103px;
    display: flex;
    justify-content: space-between;
  }

  .main__left-block {
  }

  .main__info {
    max-width: 375px;
  }

  .info__title {
    font-family: 'Intro Bold';
    font-weight: 700;
    font-size: 40px;
    line-height: 48px;
  }

  .info__text {
    margin-top: 34px;
    font-weight: 400;
    font-size: 16px;
    line-height: 24px;
    color: rgba(102, 102, 102, 1);
  }

  .info__button {
    margin-top: 30px;
    font-family: 'Intro Regular';
    font-weight: 400;
    font-size: 18px;
    background-color: transparent;
    border: none;
    color: rgba(43, 107, 243, 1);
  }

  .main__video-block {
    margin-top: 80px;
  }

  .video__title {
    font-family: 'Intro Regular';
    font-size: 22px;
    line-height: 32px;
  }

  .video-img {
    width: 100%;
    max-width: 374px;
    margin-top: 22px;
  }

  .video__pagging {
  }

  .pagging {
    width: 100%;
    display: flex;
    align-items: center;
    gap: 16px;
    margin-top: 17px;
    display: none;
  }

  .pagging__img-active {
  }

  .pagging__img {
  }

  .main__right-block {
    width: 100%;
    max-width: 360px;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .order-form {
  }

  .main__tracking {
    width: 100%;
    max-width: 360px;
    margin-top: 72px;
    background-color: rgba(255, 221, 45, 1);
    padding: 31px 20px 32px 20px;
    border-radius: 8px;
  }

  .tracking__title {
    font-family: 'Intro Regular';
    font-weight: 400;
    font-size: 22px;
    line-height: 32px;
  }

  .tracking__input-wrapper {
    width: 100%;
    margin-top: 9px;
    position: relative;
  }

  .tracking-input {
    width: 100%;
    height: 100%;
    padding: 11px 0px;
    border-radius: 8px;
    border: none;
  }

  .tracking-input::placeholder {
    padding-left: 16px;
    font-weight: 400;
    font-size: 16px;
    color: rgba(29, 37, 60, 0.6);
  }

  .tracking__loupe-img {
    position: absolute;
    right: 12px;
    top: 12px;
  }

  @media (max-width: 1000px) {
    .main-body {
      background: url('/image/main-bacground-city.png') no-repeat center bottom
        18%;
      background-color: #f1f4fc;
      padding: 32px 16px 55px 16px;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      gap: 46px;
    }
    .info__text {
      margin-top: 14px;
    }
    .info__button {
      margin-top: 14px;
    }
    .main__video-block {
      margin-top: 37px;
    }
    .video-img {
      margin-top: 17px;
    }
    .main__left-block {
      order: 1;
    }

    .main__tracking {
      margin-top: 72px;
      background-color: rgba(255, 221, 45, 1);
      padding: 23px 16px 24px 16px;
      border-radius: 8px;
    }

    .main__video-block {
    }

    .pagging {
      display: flex;
    }
  }
</style>
