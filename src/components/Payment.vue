<template>
  <section class="payment__body">
    <h3 class="payment__title">Payment methods</h3>
    <div class="payment__slider-wrapper">
      <img
        ref="left"
        src="/image/arrow-left.png"
        alt=""
        class="payment__arrow-left"
      />
      <Swiper
        :modules="modules"
        :breakpoints="{
          1000: {
            slidesPerView: 6,
            spaceBetween: 104,
            navigation: {
              prevEl: left,
              nextEl: right,
            },
          },
          0: {
            slidesPerView: 2.5,
            spaceBetween: 34,
            initialSlide: 2,
            centeredSlides: true,
          },
        }"
      >
        <SwiperSlide v-for="(icon, index) in images" :key="index">
          <img :src="icon" alt="" class="payment__slider-img" />
        </SwiperSlide>
      </Swiper>

      <img
        ref="right"
        class="payment__arrow-right"
        src="/image/arrow-right.png"
        alt=""
      />
    </div>
  </section>
</template>
<script setup lang="ts">
  import { Swiper, SwiperSlide } from 'swiper/vue'
  import 'swiper/css/navigation'
  import 'swiper/css'
  import { Navigation } from 'swiper/modules'
  import { ref } from 'vue'

  const right = ref(null)
  const left = ref(null)
  const modules = [Navigation]
  const images = [
    '/image/payment-google-pay.png',
    '/image/payment-sofort.png',
    '/image/payment-union-pay.png',
    '/image/payment-visa.png',
    '/image/payment-mastercard.png',
    '/image/payment-amex.png',
  ]
</script>
<style scoped>
  .payment__body {
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 98px 20px 96px 20px;
    min-width: 0;
  }

  .payment__title {
    width: 100%;
    white-space: nowrap;
    font-family: 'Intro Bold';
    font-weight: 700;
    font-size: 40px;
    line-height: 48px;
    text-align: center;
  }

  .payment__slider-wrapper {
    width: 100%;
    position: relative;
    margin-top: 46px;
    display: flex;
    justify-content: center;
    gap: 54px;
  }

  .payment__arrow-left {
  }

  .payment__arrow-right {
  }

  .swiper {
    margin: 0;
    max-width: 1024px;
    max-height: 56px;
  }

  .swiper-wrapper {
  }

  .swapper-slide {
  }
  .swiper-button-lock {
    display: block;
  }

  .payment__slider-img {
    max-width: 84px;
    min-height: 56px;
    width: 100%;
    height: 100%;
    object-fit: contain;
  }
  @media (max-width: 1000px) {
    .payment__body {
      padding: 54px 16px 47px 16px;
    }
    .payment__title {
      font-size: 24px;
      line-height: 32px;
    }
    .swiper {
      max-width: 360px;
      max-height: 56px;
    }
    .payment__arrow-left {
      display: none;
    }

    .payment__arrow-right {
      display: none;
    }
  }
</style>
