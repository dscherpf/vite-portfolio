<script setup>
import Page from './components/Page.vue';
import Vars from './css/vars.css';
</script>

<template>
  <page />
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
  background-color: var(--color-dark);
}
</style>
