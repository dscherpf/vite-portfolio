<template>
  <div class="project_item" :class="{ active: active }">
    <div class="project_head" v-on:click="$emit('selected')">
      <h4 class="project_head-name" v-text="project.name"></h4>
      <div class="project_head-actions">
        <a class="project_head-info">
          <mdicon class="icon" name="chevron-down" />
        </a>
        <a :href="project.link" target="_blank" class="project_head-link">
          <mdicon class="icon" name="open-in-new" />
        </a>
      </div>
    </div>
    <transition name="fade">
      <div v-if="active" class="project_body">
        <div class="project_body-content" v-html="project.description"></div>
        <div class="project_body-tags">
          <div
            v-for="(tag, i) in project.tags"
            :key="i"
            class="project_tag"
            v-text="tag"
          ></div>
        </div>
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
    active: {
      type: Boolean,
      required: true,
      default: false,
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
  margin: 0.5rem;
  display: flex;
  flex-direction: column;
  overflow: hidden;
  border-radius: var(--border-radius);
}
.project_head {
  background-color: var(--color-white);
  display: flex;
  flex-direction: row;
  align-items: stretch;
  justify-content: space-between;
  padding: 0.65rem 1rem 0.5rem;
  cursor: pointer;
}
.project_head-name {
  flex-grow: 1;
  line-height: 1.5;
  text-align: left;
}
.project_head-info {
  color: var(--color-text);
  transition: all 0.25s ease-in;
}
.active .project_head-info svg {
  transform: rotate(180deg);
  transition: all 0.25s 0.25s ease-out;
}
.project_head-link {
  color: var(--color-green);
}
.icon {
  margin: 0.25rem;
}
.project_body {
  background-color: var(--color-white);
  text-align: left;
  overflow: hidden;
}
.project_body-content {
  padding: 0 1rem;
  margin: 0.5rem 1.5rem 1.25rem;
  border-left: 2px solid var(--color-green);
}
.project_body-tags {
  display: flex;
  flex-direction: row;
  justify-content: flex-end;
  padding: 0 1rem 1rem;
}
.project_tag {
  font-size: 14px;
  border: 1px solid var(--color-green);
  border-radius: var(--border-radius);
  color: var(--color-dark);
  padding: 0.25rem 1rem;
  margin-left: 0.5rem;
}
/* animations */
.fade-enter-active,
.fade-leave-active {
  transition: all 0.25s 0.25s ease-out;
  max-height: 200px;
}

.fade-enter-from,
.fade-leave-to {
  transition: all 0.25s ease-in;
  max-height: 0px;
}
</style>
