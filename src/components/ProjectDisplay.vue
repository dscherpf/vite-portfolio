<template>
  <div class="project-container">
    <h4 class="color-white">Recent Work</h4>
    <project-item
      v-for="(project, i) in projects"
      :key="i"
      :project="project"
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
};
</script>

<style>
.project-container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  flex: 0 1 500px;
}
</style>
