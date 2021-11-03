<template>
  <div class="project_item">
    <div class="project_item-name" v-text="project.name"></div>
    <a class="project_item-info">
      <mdicon class="icon" name="information-outline" />
    </a>
    <a :href="project.link" target="_blank" class="project_item-link">
      <mdicon class="icon" name="open-in-new" />
    </a>
  </div>
</template>

<script>
import { mdiInformationOutline } from '@mdi/js';
export default {
  name: 'project-item',
  props: {
    project: {
      type: Object,
      required: true,
    },
  },
  data() {
    return {
      info: mdiInformationOutline,
    };
  },
};
</script>

<style>
.project_item {
  background-color: var(--color-white);
  display: flex;
  flex-direction: row;
  align-items: stretch;
  margin: 0.5rem;
  padding: 0.5rem 1rem;
}
.project_item-name {
  flex-grow: 1;
  text-align: left;
}
.icon {
  margin: 0.25rem;
}
</style>
