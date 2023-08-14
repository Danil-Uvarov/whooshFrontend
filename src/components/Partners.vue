<template>
  <section class="partners__body">
    <div class="partners__title-wrapper">
      <div class="partners__plug" />
      <h2 class="parters__title">Our Partners</h2>
      <PartnersButton class="partners__button-ps" />
    </div>
    <Swiper
      :breakpoints="{
        1000: {
          direction: 'horizontal',
          spaceBetween: 80,
          slidesPerView: 5,
          autoHeight: true,
        },
        0: {
          direction: 'horizontal',
          spaceBetween: 44,
          slidesPerView: 2,
          autoHeight: true,
          centeredSlides: true,
          initialSlide: 2,
        },
      }"
    >
      <SwiperSlide v-for="(partner, index) in partners" :key="index">
        <img
          :src="getPhoto(index)"
          alt=""
          class="partners-image"
          @mouseenter="hovered(index)"
          @mouseleave="noHovered"
        />
      </SwiperSlide>
    </Swiper>
    <PartnersButton class="partners__button-phone" />
  </section>
</template>
<script setup lang="ts">
  import { Swiper, SwiperSlide } from 'swiper/vue'
  import PartnersButton from './buttons/PartnersButton.vue'
  import { ref } from 'vue'

  const getPhoto = (index: number) => {
    if (active.value === index) {
      return partners[index].activeImage
    }
    return partners[index].image
  }
  const active = ref<number | null>(null)
  const hovered = (index: number) => {
    active.value = index
  }
  const noHovered = () => {
    active.value = null
  }
  const partners = [
    {
      image: '/image/partner-alva.png',
      activeImage: '/image/partner-alva-active.svg',
    },
    {
      image: '/image/partner-tendo.png',
      activeImage: '/image/partner-tendo-active.svg',
    },
    {
      image: '/image/partner-fagor.png',
      activeImage: '/image/partner-fagor-active.svg',
    },
    {
      image: '/image/partner-radioShack.png',
      activeImage: '/image/partner-radioShack-active.svg',
    },
    {
      image: '/image/partner-gitarCenter.png',
      activeImage: '/image/partner-gitarCenter-active.svg',
    },
  ]
</script>
<style scoped>
  .swiper {
    width: 100%;
    margin-top: 70px;
    max-width: 1104px;
  }
  .partners__body {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: 98px 0 47px 0;
    min-width: 0;
  }

  .partners__plug {
    width: 254px;
  }

  .partners__button-phone {
    display: none;
  }

  .partners__button-ps {
    display: flex;
  }

  .partners__title-wrapper {
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: space-around;
  }

  .parters__title {
    white-space: nowrap;
    font-family: 'Intro Bold';
    font-weight: 700;
    font-size: 40px;
    line-height: 48px;
  }

  .partners__images {
    margin-top: 70px;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 88px;
  }

  .partners-image {
    max-width: 188px;
    max-height: 57px;
    width: 100%;
    object-fit: contain;
  }

  .partners__button-phone {
    display: none;
  }

  @media (max-width: 1000px) {
    .partners__body {
      display: flex;
      flex-direction: column;
      padding: 38px 16px 47px 16px;
    }

    .partners__title-wrapper {
      margin: 0 auto;
      display: flex;
      align-items: center;
    }

    .parters__title {
      white-space: nowrap;
      font-family: 'Intro Bold';
      font-weight: 700;
      font-size: 40px;
      line-height: 48px;
      text-align: center;
    }

    .partners__button-blcock {
      margin: 0 50%;
      white-space: nowrap;
      display: flex;
      align-items: center;
      justify-content: center;
      float: right;
      gap: 9px;
      background-color: transparent;
      border: 1px solid rgba(221, 231, 253, 1);
      border-radius: 24px;
      padding: 8px 16px;
    }

    .button__img {
    }

    .button__text {
      font-size: 16px;
    }

    .partners__images {
      margin-top: 70px;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 88px;
    }

    .partners-image {
    }

    .partners__button-phone {
      display: block;
      margin-top: 48px;
      padding: 0 58px;
    }

    .partners__plug {
      display: none;
    }

    .partners__button-ps {
      display: none;
    }
    .swiper {
      max-width: 360px;
      margin-top: 26px;
    }
  }
</style>
