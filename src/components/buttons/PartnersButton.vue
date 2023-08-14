<template>
  <button class="partners__button-blcock button">
    <img src="image/partners-button.png" alt="" class="button__img" />
    <span class="button__text" :style="{ active: isActive }" @mouseenter="style"
      >Let's collaborate</span
    >
  </button>
</template>
<script setup lang="ts">
  import { ref } from 'vue'

  const isActive = ref(0)
  const style = () => {
    isActive.value = 1
  }
</script>
<style scoped>
  .active {
    background-color: red;
  }

  .partners__button-blcock {
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
