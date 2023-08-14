<template>
  <header class="header">
    <section class="header__wrapper">
      <div class="header-logo__city">
        <img
          src="/image/header-logo.png"
          alt=""
          class="header__logo-img"
        >
        <div class="header__city-block city">
          <img
            src="/image/header-location.png"
            alt=""
            class="city-img"
          >
          <span class="city">NY. Manhattan</span>
        </div>
      </div>
      <div class="header__search search">
        <input
          type="text"
          class="search-input"
          placeholder="Track a Package"
        >
        <img
          src="/image/header-input-loupe.png"
          alt=""
          class="searh-loupe"
        >
      </div>
      <div class="header__navbar-wrapper navbar">
        <nav class="navbar-block ">
          <ul class="navbar__list">
            <li class="navbar__link">
              <a href="">{{ navbarItems[0] }}</a>
            </li>
            <li class="navbar__link">
              <a href="">{{ navbarItems[1] }}</a>
            </li>
          </ul>
        </nav>
        <img
          src="/image/header-login.png"
          alt=""
          class="navbar__login-img"
        >
      </div>
    </section>
    <Burger
      class="header__burger"
      :navbar-items="navbarItems"
    />
  </header>
</template>
<script setup lang ="ts">
import Burger from './menu/Burger.vue'

const navbarItems = [
  'Send a Parcel',
  'Become a Courier',
  'Affiliate Program',
  'Help & Support'
]
</script>
<style scoped>
.header {
  background-color: #F1F4FC;
  border-bottom: 2px solid #C2D2F4;
}

.header__wrapper {
  padding: 0px 32px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.header-logo__city {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 66px;
}

.header__logo-img {
  width: 100%;
  max-width: 192px;
  max-height: 64px;
}

.header__city-block {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 6px;
}

.city {
  white-space: nowrap;
  font-weight: 400;
  font-size: 16px;
  line-height: 24px;
  color: #666666;
}

.city-img {}

.header__search {
  position: relative;
  margin: 0 auto;
}


.search-input {
  border-radius: 8px;
  border: solid 1px #C2D2F4;
  padding: 12px 34px 12px 16px;
}

.search-input::placeholder {
  font-weight: 400;
  font-size: 14px;
  line-height: 24px;
  color: rgba(29, 37, 60, 0.6);
}

.searh-loupe {
  right: 12px;
  top: 14px;
  position: absolute;
  z-index: 2;
}


.header__navbar-wrapper {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 32px;
}

.navbar {}

.navbar-block {
  margin: 0px;
  padding: 0px;
}

.navbar__list {
  list-style: none;
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 36px;
}

.navbar__link {}

.navbar__link a {
  text-decoration: none;
  white-space: nowrap;
  font-weight: 400;
  font-size: 16px;
  line-height: 24px;
  color: #666666;
}

.navbar__login-img {
  max-width: 40px;
  max-height: 40px;
}

.header__burger {
  display: none;
}

@media(max-width: 1000px) {
  .header {}

  .header__wrapper {
    display: none;
  }

  .header__burger {
    display: flex;

  }
}
</style>
