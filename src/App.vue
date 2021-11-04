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
  background-size: 1750px;
  /* min-height: calc(100vh - 20px); */
  min-height: 100vh;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}
body {
  margin: 0;
  background-color: var(--color-dark);
  /* border: 10px solid var(--color-green); */
}
</style>
