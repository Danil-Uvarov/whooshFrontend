<template>
  <footer class="footer__body">
    <section class="footer__wrapper">
      <div class="footer__content">
        <div class="footer__description description">
          <h3 class="description__title">About Whoosh</h3>
          <div class="description__block-content">
            <img
              src="/image/footer-symbol.svg"
              alt=""
              class="description__image"
            />
            <p class="description__text">
              Express delivery of documents and parcels for organizations,
              express delivery of correspondence, purchases and other goods
            </p>
          </div>
        </div>
        <nav class="footer__navigation navigation">
          <div class="navigation__menu">
            <h3 class="navigation__title">Menu</h3>
            <div class="navigation__link-line" />
            <ul class="navigation__list">
              <li class="navigation__link">About company</li>
              <li class="navigation__link">Contact</li>
              <li class="navigation__link">Rules</li>
              <li class="navigation__link">FAQ</li>
              <li class="navigation__link">Reviews</li>
              <li class="navigation__link">Cargo transportation</li>
              <li class="navigation__link">Tariffs</li>
            </ul>
          </div>
          <div class="navigation__services">
            <h3 class="navigation__title">Services</h3>
            <div class="navigation__link-line" />
            <ul class="navigation__list">
              <li class="navigation__link">Online stores</li>
              <li class="navigation__link">Legal entity</li>
              <li class="navigation__link">API Integration</li>
              <li class="navigation__link">Contract</li>
              <li class="navigation__link">Jobs</li>
              <li class="navigation__link">Courier job</li>
              <li class="navigation__link">The blog</li>
            </ul>
          </div>
        </nav>
        <nav class="footer__contacts contacts">
          <h3 class="contacts__title">Contact us</h3>
          <div class="contacts__line" />
          <a class="contacts__number" href="tel:+78009345959">8 800 934 5959</a>
          <div class="contacts__location-wrapper">
            <img
              src="/image/footer-contacts.png"
              alt=""
              class="contacts__location-img"
            />
            <div class="contacts__location-strings">
              <span>2545 W. Diversey Ave. </span>
              <span>3rd Floor Chicago, IL 60647</span>
            </div>
          </div>
          <div class="contacts__socials">
            <img
              src="/image/footer-facebook.png"
              alt=""
              class="contacts__social-img"
            /><img
              src="/image/footer-vk.png"
              alt=""
              class="contacts__social-img"
            /><img
              src="/image/footer-youtube.png"
              alt=""
              class="contacts__social-img"
            /><img
              src="/image/footer-instagram.png"
              alt=""
              class="contacts__social-img"
            />
          </div>
        </nav>
      </div>

      <div class="footer-line-wrapper">
        <div class="footer__line" />
        <span class="footer__line-text">Made by</span>
      </div>

      <div class="footer__secondary secondary">
        <h5 class="secondary__copyright">© 2022. All rights reserved.</h5>
        <img src="/image/footer-logo.png" alt="" class="secondary__image" />
        <div class="secondary__policy-block policy">
          <img
            src="/image/footer-policy.svg"
            alt=""
            class="policy__image-logo"
          />
          <h5 class="policy__text">Privacy policy</h5>
        </div>
      </div>
      <img
        src="/image/footer-logo-phone.svg"
        alt=""
        class="footer__logo-phone"
      />
    </section>
  </footer>
</template>
<script setup lang="ts"></script>
<style scoped>
  .footer__body {
    width: 100%;
    background-color: #f1f4fc;
  }
  .footer__wrapper {
    width: 100%;
    max-width: 1160px;
    margin: 0 auto;
    padding: 85px 130px 56px 103px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }
  .footer__content {
    width: 100%;
    display: flex;
    justify-content: space-between;
  }
  .footer__description {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .description__title {
    font-family: 'Intro Bold';
    font-weight: 700;
    font-size: 14px;
    line-height: 16px;
  }
  .description__block-content {
    margin-top: 32px;
    display: flex;
    justify-content: center;
    gap: 16px;
  }
  .description__image {
    width: 100%;
    max-width: 44px;
  }
  .description__text {
    width: 100%;
    max-width: 240px;
    font-weight: 400;
    font-size: 14px;
    color: rgba(29, 37, 60, 0.7);
  }
  .footer__navigation {
    display: flex;
    justify-content: center;
    gap: 69px;
  }
  .navigation__menu {
    width: 100%;
    max-width: 200px;
    display: flex;
    flex-direction: column;
  }
  .navigation__services {
    width: 100%;
    max-width: 200px;
    display: flex;
    flex-direction: column;
  }

  .navigation__title {
    font-family: 'Intro Bold';
    font-weight: 700;
    font-size: 14px;
    line-height: 16px;
  }
  .navigation__link-line {
    margin-top: 9px;
    width: 100%;
    height: 2px;
    background-color: rgba(183, 198, 231, 1);
  }
  .navigation__list {
    margin-top: 21px;
    width: 100%;
    height: 100%;
    max-width: 145px;
    max-height: 224px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
  .navigation__link {
    list-style: none;
    font-weight: 400;
    font-size: 14px;
    line-height: 32px;
  }
  .footer__contacts {
    display: flex;
    flex-direction: column;
    width: 100%;
    max-width: 232px;
  }
  .contacts__title {
    font-family: 'Intro Bold';
    font-weight: 700;
    font-size: 14px;
    line-height: 16px;
  }
  .contacts__line {
    margin-top: 9px;
    width: 100%;
    height: 2px;
    background-color: rgba(183, 198, 231, 1);
  }
  .contacts__number {
    margin-top: 22px;
    font-family: 'Intro Bold';
    font-weight: 700;
    font-size: 24px;
    line-height: 32px;
    text-decoration: none;
    color: rgba(29, 37, 60, 1);
  }
  .contacts__location-wrapper {
    margin-top: 23px;
    display: flex;
    justify-content: center;
    gap: 12px;
  }
  .contacts__location-img {
    width: 100%;
    max-width: 12px;
    max-height: 16px;
  }
  .contacts__location-strings {
    display: flex;
    flex-direction: column;
    gap: 12px;
  }
  .contacts__socials {
    margin-top: 68px;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  .contacts__social-img {
    width: 100%;
    max-width: 40px;
  }

  .footer-line-wrapper {
    margin-top: 25px;
    width: 100%;
    position: relative;
  }
  .footer__line {
    margin-top: 25px;
    width: 100%;
    height: 2px;
    background-color: rgba(194, 210, 244, 1);
  }
  .footer__line-text {
    padding: 0 11px;
    position: absolute;
    top: 15px;
    left: 50%;
    margin-left: -10px;
    text-align: center;
    z-index: 2;
    color: rgba(183, 198, 231, 1);
    background-color: #f1f4fc;
  }
  .footer__secondary {
    width: 100%;
    margin-top: 24px;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .secondary__copyright {
    font-weight: 400;
    font-size: 14px;
  }
  .secondary__image-logo {
  }
  .secondary__policy-block {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 13px;
  }

  .policy__image {
    width: 100%;
    max-width: 10px;
  }
  .policy__text {
    font-weight: 400;
    font-size: 14px;
  }
  .footer__logo-phone {
    display: none;
  }
  @media (max-width: 1200px) {
    .footer__wrapper {
      width: 100%;
      max-width: 360px;
      padding: 45px 16px 32px 16px;
    }
    .footer__content {
      flex-direction: column;
      align-items: start;
    }
    .footer__description {
      align-items: start;
    }

    .footer__navigation {
      margin-top: 32px;
      display: flex;
      justify-content: space-between;
    }

    .footer__contacts {
      margin-top: 42px;
      display: flex;
      flex-direction: column;
      align-items: start;
      width: 100%;
      max-width: 100%;
    }

    .contacts__socials {
      margin-top: 68px;
      width: 100%;
      display: flex;
      align-items: center;
      justify-content: space-around;
    }

    .footer-line-wrapper {
      order: 2;
    }

    .footer__line {
      margin-top: 33px;
    }
    .footer__line-text {
      top: 25px;
      margin-left: -40px;
    }
    .footer__secondary {
      width: 100%;
      margin-top: 53px;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      gap: 24px;
    }
    .secondary__copyright {
      order: 2;
    }

    .secondary__image {
      display: none;
    }

    .footer__logo-phone {
      margin: 0 auto;
      margin-top: 32px;
      display: block;
      order: 3;
    }
  }
</style>
