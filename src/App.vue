<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld msg="NadetDev Vue.js App" />
  <HomeComponent msg="NadetDev Vue.js Primer App" />
  <HomeCounter message="by NadetDev" />
</template>

<script>
import HomeComponent from './components/HomeComponent.vue';
import MyCounter from './components/MyCounter';

export default {
  name: 'App',
  components: {
    HomeComponent,
    HomeCounter: MyCounter,
  },
};
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
