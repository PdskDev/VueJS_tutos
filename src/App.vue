<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <HomeComponent msg="NadetDev Vue.js Primer App" />
  <HomeCounter />
</template>

<script setup>
import HomeComponent from './components/HomeComponent.vue';
import HomeCounter from './components/MyCounter';
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
