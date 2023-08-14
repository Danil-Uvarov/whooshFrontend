<template>
  <section class="description__body">
    <div class="description__text-wrapper">
      <p>
        We make delivery exactly at the time you need - we can start to fulfill
        the order a few minutes after it arrives, or we can deliver on a
        specific day and hour.
      </p>

      <p v-show="isActive" class="description__text">
        <span>
          Since 2019, LibertyWalk has successfully provided express courier
          delivery services in the city for both individuals and legal entities,
          and is also a reliable logistics partner for delivery services for
          online stores and restaurants! Express delivery of documents and
          parcels for organizations, express delivery of correspondence,
          purchases, flowers, food, gifts and goods up to 1.5 tons - the most
          frequent orders in our company.
        </span>
        <span>
          But at the same time, we do not limit the range of courier services
          and without problems we can buy and bring goods and products from the
          online store, arrange delivery for the online store, cafe,
          supermarket, restaurant or any other business. Around the clock on our
          website you can call a courier in just a minute and arrange an express
          courier delivery without unnecessary bureaucracy, negotiations and
          calls to the call center.
        </span>
      </p>
      <button class="description__button" @click="isActive = !isActive">
        <img src="/image/description-button.png" alt="" />
      </button>
    </div>
  </section>
</template>
<script setup lang="ts">
  import { ref } from 'vue'

  const isActive = ref(false)
</script>
<style scoped>
  .description__body {
    padding: 100px 16px 84px 16px;
    max-width: 1160px;
    width: 100%;
    margin: 0 auto;
  }

  .description__text-wrapper {
    display: flex;
    flex-direction: column;
    color: rgba(102, 102, 102, 0.7);
  }

  .description__text {
    margin-top: 10px;
    display: flex;
    flex-direction: column;
    gap: 20px;
  }

  .description__text p {
    font-weight: 400;
    font-size: 16px;
  }

  .description__button {
    text-align: right;
    border: none;
    background-color: #ffff;
  }
  @media (max-width: 1000px) {
    .description__body {
      padding: 54px 16px 52px 16px;
    }
  }
</style>
