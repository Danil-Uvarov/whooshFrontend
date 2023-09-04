<template>
  <div class="burger">
    <section key="menu" class="burger__header-wrapper">
      <img src="/image/burger-profile.png" alt="" class="burger__img-profile" />
      <img src="/image/header-logo.png" alt="" class="burger__logo-img" />
      <button class="burger__menu-button" @click="open = !open">
        <span class="burger-button__line" />
      </button>
    </section>
    <section v-if="open" class="burger-menu">
      <div class="burger-citu__close">
        <div class="burger__city-block city">
          <img src="/image/header-location.png" alt="" class="city-img" />
          <span class="city-text">NY, Manhattan</span>
        </div>
        <span key="menu" class="burger__close menu" @click="open = !open" />
      </div>
      <div class="burger__search search">
        <input type="text" class="search-input" placeholder="Track a Package" />
        <img src="/image/header-input-loupe.png" alt="" class="searh-loupe" />
      </div>
      <nav class="burger__navbar-block navbar">
        <ul class="navbar__list">
          <li
            v-for="(item, index) in navbarItems"
            :key="index"
            class="navbar__link"
          >
            <a href="">{{ item }}</a>
          </li>
        </ul>
      </nav>
      <button class="burger-button">Take a complex order</button>
    </section>
  </div>
</template>
<script setup lang="ts">
  import { ref } from 'vue'

  const open = ref(false)
  interface props {
    navbarItems: object
  }
  defineProps<props>()
</script>
<style scoped>
  .burger {
    position: relative;
  }

  .burger__header-wrapper {
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .burger__img-profile {
    width: 100%;
    max-width: 24px;
    max-height: 24px;
  }

  .burger__logo-img {
    width: 100%;
    max-width: 120px;
    max-height: 40px;
  }

  .burger__menu-button {
    border: solid 1px #f1f4fc;
    background-color: #f1f4fc;
    display: flex;
    flex-direction: column;
    align-items: end;
    gap: 3px;
  }

  .burger-button__line {
    display: block;
    width: 18px;
    height: 3px;
    background-color: #b7c6e7;
    position: relative;
  }

  .burger-button__line::before {
    content: '';
    display: block;
    position: absolute;
    width: 14px;
    height: 3px;
    top: 6px;
    right: 0px;
    background-color: #b7c6e7;
  }

  .burger-button__line::after {
    content: '';
    display: block;
    position: absolute;
    width: 18px;
    height: 3px;
    bottom: 6px;
    right: 0px;
    background-color: #b7c6e7;
  }

  .burger-menu {
    position: absolute;
    right: 0px;
    top: 0px;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 24px 16px 32px 16px;
    background-color: #ffffff;
  }

  .burger-citu__close {
    width: 100%;
    display: flex;
    justify-content: space-between;
  }

  .burger__city-block {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 6px;
  }

  .city-text {
    font-weight: 400;
    font-size: 16px;
    color: #666666;
    border-bottom: 1px dashed #b7c6e7;
  }

  .city-img {
    max-width: 12px;
    max-height: 16px;
  }

  .burger__close {
    position: relative;
    width: 24px;
    height: 24px;
    opacity: 0.3;
  }

  .burger__close::before,
  .burger__close::after {
    position: absolute;
    left: 15px;
    content: ' ';
    height: 19px;
    width: 2px;
    background-color: #b7c6e7;
  }

  .burger__close:before {
    transform: rotate(45deg);
  }

  .burger__close:after {
    transform: rotate(-45deg);
  }

  .burger__search {
    width: 100%;
    margin-top: 40px;
    position: relative;
  }

  .search-input {
    border-radius: 8px;
    border: solid 1px #c2d2f4;
    width: 100%;
    padding: 8px 16px;
    width: 242px;
  }

  .search-input::placeholder {
    font-weight: 400;
    font-size: 14px;
    line-height: 24px;
    color: rgba(29, 37, 60, 0.479);
  }

  .searh-loupe {
    right: 12px;
    top: 8px;
    position: absolute;
    z-index: 2;
  }

  .burger__navbar-block {
    width: 100%;
    margin-top: 44px;
  }

  .navbar__list {
    display: flex;
    flex-direction: column;
    gap: 24px;
  }

  .navbar__link {
    list-style: none;
  }

  .navbar__link a {
    text-decoration: none;
    font-weight: 400;
    font-size: 16px;
    line-height: 24px;
    color: #666666;
  }

  .burger-button {
    font-family: 'Intro-regular';
    margin-top: 220px;
    text-align: center;
    font-weight: 400;
    padding: 16px 28px;
    font-size: 18px;
    line-height: 32px;
    border-radius: 32px;
    border: 1px solid #ffffff;
    background-color: #2b6bf3;
    color: #ffffff;
  }
</style>
