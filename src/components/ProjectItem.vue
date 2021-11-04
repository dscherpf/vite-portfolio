<template>
  <div class="project_item">
    <div class="project_head" v-on:click="active = !active">
      <div class="project_head-name" v-text="project.name"></div>
      <div class="project_head-actions">
        <a class="project_head-info">
          <mdicon class="icon" name="information-outline" />
        </a>
        <a :href="project.link" target="_blank" class="project_head-link">
          <mdicon class="icon" name="open-in-new" />
        </a>
      </div>
    </div>
    <transition name="fade">
      <div v-if="active" class="project_body">
        <div class="project_body-content" v-html="project.description"></div>
      </div>
    </transition>
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
      active: false,
    };
  },
};
</script>

<style>
.project_item {
  background-color: var(--color-white);
  margin: 0.5rem;
}
.project_head {
  display: flex;
  flex-direction: row;
  align-items: stretch;
  justify-content: space-between;
  padding: 0.5rem 1rem;
  cursor: pointer;
}
.project_head-name {
  font-weight: bold;
  flex-grow: 1;
  line-height: 1.5;
  text-align: left;
  text-transform: uppercase;
}
.project_head-link {
  color: var(--color-green);
}
.icon {
  margin: 0.25rem;
}
.project_body {
  padding: 1rem;
  text-align: left;
}
</style>
