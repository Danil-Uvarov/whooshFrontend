<template>
  <button class="partners__button-block button">
    <img src="/image/partners-button.png" alt="" class="button__img" />
    <span class="button__text">Let's collaborate</span>
  </button>
</template>
<script setup lang="ts"></script>
<style scoped>
  .partners__button-block {
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
</style>
