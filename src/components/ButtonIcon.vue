<template>
  <div class="button-icon">
    <a :href="link" target="_blank">
      <!-- <img :src="image" :alt="alt" /> -->
      <component :is="selectedIcon" />
    </a>
  </div>
</template>

<script>
import IconGithub from './icons/IconGithub.vue';
import IconLinkedin from './icons/IconLinkedin.vue';
export default {
  name: 'ButtonIcon',
  components: { IconGithub, IconLinkedin },
  props: {
    link: {
      type: String,
      required: true,
    },
    icon: {
      type: String,
      required: true,
    },
  },
  computed: {
    selectedIcon() {
      switch (this.icon) {
        case 'github':
          return 'IconGithub';
        case 'linkedin':
          return 'IconLinkedin';
      }
    },
  },
};
</script>

<style>
.button-icon {
  background-color: var(--color-white);
  border-radius: var(--border-radius);
  height: 40px;
  width: 40px;
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 0 0.5rem;
  opacity: 0.65;
}
.button-icon:hover {
  opacity: 1;
}
.button-icon a {
  display: flex;
}
.button-icon img {
  height: 35px;
}
</style>
