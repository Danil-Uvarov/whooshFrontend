<template>
  <form action="#" method="post" class="order-form form">
    <div class="form-titlte__tooltip">
      <h2 class="form__title">Send a Parcel</h2>
      <div class="form__tooltip-img-wrapper">
        <img src="/image/tooltip.png" class="form__tooltip-img" />
        <Tooltip class="form__tooltip-active" :text="text" />
      </div>
    </div>
    <nav class="form__tabs-block tabs">
      <ul class="tabs__list">
        <li
          v-for="(tab, index) in tabs"
          :key="index"
          class="tabs__link"
          :class="{ active: index === currentTab }"
          @click="changeTab(index)"
        >
          <img :src="tab.icon" alt="" class="tab__img-foot" />
          <h5 class="tubs-text">
            {{ tab.text }}
          </h5>
        </li>
      </ul>
    </nav>
    <div class="form__location-wrapper location">
      <div class="location__arrow-block">
        <img
          class="location__arrow-img-pad"
          src="/image/tabs-pin-circle.png"
          alt=""
        />
        <img
          class="location__arrow-img-line"
          src="/image/tabs-pin-line.png"
          alt=""
        />
        <img
          class="location__arrow-img-ellipse"
          src="/image/tabs-pin-arrow.png"
          alt=""
        />
      </div>
      <div class="location__inputs-body">
        <div class="location__block-input">
          <span class="location__title">Pickup location</span>
          <input class="location__input" type="text" placeholder="location" />
        </div>
        <div class="location__block-input">
          <span class="location__title">Pickup location</span>
          <input
            class="location__input"
            type="text"
            placeholder="502 86th St, Brooklyn, NY 11209"
          />
        </div>
      </div>
    </div>
    <button class="form__open">Order</button>
    <button class="form__clear" type="reset">
      <img src="/image/form-clear.png" alt="" class="form__clear-image" /> Clear
      All
    </button>
  </form>
</template>
<script setup lang="ts">
  import Tooltip from './Tooltip.vue'
  import { ref } from 'vue'

  const currentTab = ref(0)
  const changeTab = (index: number) => {
    currentTab.value = index
  }
  const tabs = [
    {
      icon: '/image/tabs-foot.svg',
      text: 'up to 10lb',
    },
    {
      icon: ' /image/tabs-car.png',
      text: 'up to 130lb',
    },
    {
      icon: '/image/tabs-truck.png',
      text: 'over 130lb',
    },
  ]
  const text =
    'A commission is a piece of work that someone is asked to do and is paid'
</script>

<style scoped>
  .order-form {
    width: 100%;
    border-radius: 10px;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 39px 32px 24px 32px;
    background-color: #fff;
    border: 2px solid rgba(183, 198, 231, 1);
  }

  .form-titlte__tooltip {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 16px;
  }

  .form__title {
    font-family: 'Intro-Regular';
    font-weight: 400;
    font-size: 22px;
    line-height: 32px;
    color: rgba(29, 37, 60, 1);
  }

  .form__tooltip-img-wrapper {
    max-width: 24px;
    max-height: 24px;
    position: relative;
  }

  .form__tooltip-img {
  }

  .form__tooltip-active {
    display: none;
  }

  .form__tooltip-img-wrapper:hover .form__tooltip-active {
    display: flex;
  }

  .form__tabs-block {
    width: 100%;
  }

  .tabs__list {
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    border: none;
    margin-top: 20px;
  }

  .tabs__link {
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    list-style: none;
    max-width: 100px;
    box-sizing: border-box;
    position: relative;
    padding: 8px 16px;
    background-color: rgba(239, 244, 255, 1);
    border: 1px solid rgba(183, 198, 231, 1);
    border-radius: 8px;
    color: rgba(29, 37, 60, 0.5);
  }
  .tab__img-foot {
  }

  .active {
    background-color: #fff;
    border-radius: 0px;
    border: 2px solid rgba(43, 107, 243, 1);
    color: #000;
  }

  .tubs-text {
    width: 100%;
    font-weight: 400;
    font-size: 12px;
    white-space: nowrap;
  }

  .form__location-wrapper {
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-top: 34px;
    gap: 16px;
  }

  .location__arrow-block {
    display: flex;
    flex-direction: column;
    justify-content: center;
  }

  .location__arrow-img-pad {
    margin-top: 16px;
  }

  .location__arrow-img-line {
    max-height: 52px;
    max-width: 4px;
    margin: 0 auto;
    margin-top: 8px;
  }

  .location__arrow-img-ellipse {
    margin-top: 4px;
  }

  .location__inputs-body {
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    gap: 37px;
  }

  .location__block-input {
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    gap: 7px;
  }

  .location__title {
    font-family: 'Intro-bold';
    font-weight: 700;
    font-size: 12px;
    line-height: 16px;
    text-transform: uppercase;
    border: 1px solid #ffff;
    color: rgba(29, 37, 60, 0.5);
  }

  .location__input {
    width: 100%;
    height: 20px;
    border: 1px solid #ffff;
    display: inline-block;
    padding-bottom: 2px;
    border-bottom: 2px solid rgba(43, 107, 243, 0.16);
    color: rgba(29, 37, 60, 0.7);
  }

  .location__input:focus {
    font-weight: 400;
    font-size: 16px;
    line-height: 24px;
    color: rgba(29, 37, 60, 1);
    outline: none;
    border-bottom: 2px solid blue;
  }

  .location__input::placeholder {
    font-weight: 400;
    font-size: 16px;
    line-height: 24px;
  }

  .form__open {
    font-family: 'Intro-regular';
    margin-top: 40px;
    width: 100%;
    border-radius: 32px;
    border: none;
    background-color: rgba(43, 107, 243, 1);
    color: #ffff;
    padding: 8px 0px;

    font-weight: 400;
    font-size: 18px;
  }

  .form__clear {
    margin-top: 16px;
    font-weight: 400;
    font-size: 16px;
    line-height: 24px;
    background-color: #ffff;
    border: none;
    color: rgba(153, 153, 153, 1);
  }

  .input:checked .tabs__link {
    background-color: red;
    display: block;
  }
  @media (max-width: 1000px) {
    .order-form {
      padding: 39px 16px 24px 16px;
    }
    .tubs-text {
      display: none;
    }
  }
</style>
