<script setup>
import NamePlate from './components/NamePlate.vue';
import Vars from './css/vars.css';
</script>

<template>
  <NamePlate />
</template>

<style>
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  background-image: url(./assets/Background.jpg);
  min-height: 100vh;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}
body {
  margin: 0;
}
</style>
