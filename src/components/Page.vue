<template>
  <div class="container">
    <name-plate />
    <project-display />
  </div>
</template>

<script>
import NamePlate from './NamePlate.vue';
import ProjectDisplay from './ProjectDisplay.vue';

export default {
  name: 'page',
  components: { NamePlate, ProjectDisplay },
};
</script>

<style>
.container {
  display: flex;
  flex-direction: column;
}
@media (min-width: 960px) {
  .container {
    width: 1080px;
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    align-items: center;
  }
}
</style>
