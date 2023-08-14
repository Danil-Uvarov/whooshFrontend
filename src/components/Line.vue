<template>
  <section class="line__body">
    <div class="line" />
    <img src="../../public/image/line-block.png" alt="" class="line__img" />
  </section>
</template>
<script setup lang="ts"></script>
<style scoped>
  .line__body {
    width: 100%;
    position: relative;
  }

  .line {
    width: 100%;
    height: 2px;
    background-color: rgba(183, 198, 231, 1);
  }

  .line__img {
    background-color: #fff;
    padding: 0px 50px;
    position: absolute;
    margin-left: auto;
    margin-right: auto;
    top: -14px;
    left: 50%;
    margin-left: -66px;
    text-align: center;
    z-index: 2;
  }
</style>
