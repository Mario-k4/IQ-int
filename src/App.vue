<script setup>
import { RouterView } from 'vue-router';
import TheNavbar from './components/TheNavbar.vue'
import TheFooter from './components/TheFooter.vue'


</script>
<template>
  <!-- <div class="container"> -->
  <TheNavbar />
  <RouterView />
  <TheFooter />
  <!-- </div> -->
</template>

<style>
/* .container {
  width: 100%;
  margin: 0;
  padding: 0;
  box-sizing: border-box;
} */
</style>