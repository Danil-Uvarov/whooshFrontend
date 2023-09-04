<template>
  <div class="tooltip">
    <div class="tooltip-img-active">i</div>
    <span class="tooltip-text">{{ text }} </span>
  </div>
</template>
<script setup lang="ts">
  defineProps<{
    text: string
  }>()
</script>
<style scoped>
  .tooltip {
    justify-content: center;
    align-items: center;
    right: -51px;
    top: -16px;
    position: absolute;
    width: 252px;
    height: 174px;
    z-index: 2;
  }

  .tooltip-img-active {
    padding: 2px 10px;
    background-color: #000000;
    color: #fff;
    border-radius: 100%;
    position: absolute;
    top: 16px;
    right: 19px;
  }

  .tooltip-text {
    padding: 8px 16px;
    background-color: #fff;
    font-weight: 400;
    font-size: 14px;
    color: rgba(29, 37, 60, 1);
    border: 1px solid rgba(183, 198, 231, 1);
    box-shadow: 1px 16px 16px rgba(73, 99, 176, 0.2);
  }
</style>
