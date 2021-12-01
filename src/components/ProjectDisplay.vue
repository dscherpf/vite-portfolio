<template>
  <div class="project-container">
    <h3 class="color-white">Recent Work</h3>
    <project-item
      v-for="(project, i) in projects"
      :key="i"
      :project="project"
      :active="model === i ? true : false"
      v-on:selected="model === i ? (model = null) : (model = i)"
    />
  </div>
</template>

<script>
import ProjectData from '../content/projects.json';
import ProjectItem from './ProjectItem.vue';
export default {
  components: { ProjectItem },
  name: 'project-display',
  computed: {
    projects() {
      return ProjectData;
    },
  },
  data() {
    return {
      model: null,
    };
  },
};
</script>

<style>
.project-container {
  display: flex;
  flex-direction: column;
  justify-content: center;
}
@media (min-width: 960px) {
  .project-container {
    flex: 0 1 500px;
  }
}
</style>
