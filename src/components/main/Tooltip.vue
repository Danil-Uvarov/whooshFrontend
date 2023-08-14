<template>
  <div class="tooltip">
    <div class="tooltip-img-active">i</div>
    <span class="tollip-text"
      >A commission is a piece of work that someone is asked to do and is paid
    </span>
  </div>
</template>
<script setup lang="ts"></script>
<style scoped>
  .tooltip {
    justify-content: center;
    align-items: center;
    right: -51px;
    top: -16px;
    position: absolute;
    border: 1px dashed rgba(151, 71, 255, 1);
    text-align: center;
    width: 295px;
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

  .tollip-text {
    padding: 8px 16px;
    background-color: #fff;
    font-weight: 400;
    font-size: 14px;
    color: rgba(29, 37, 60, 1);
  }
</style>
