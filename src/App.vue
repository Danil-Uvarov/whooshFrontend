<template>
  <div class="app">
    <TheHeader />
    <Main />
    <Info />
    <Line />
    <Partners />
    <Intro></Intro>
    <Payment></Payment>
    <Line></Line>
    <Description></Description>
    <TheFooter></TheFooter>
  </div>
</template>

<script setup lang="ts">
  import TheHeader from './components/TheHeader.vue'
  import Main from './components/Main.vue'
  import Info from './components/Info.vue'
  import Line from './components/Line.vue'
  import Partners from './components/Partners.vue'
  import Intro from './components/Intro.vue'
  import Payment from './components/Payment.vue'
  import Description from './components/Description.vue'
  import TheFooter from './components/TheFooter.vue'
</script>
<style scoped></style>
