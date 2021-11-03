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
  border-radius: 100%;
  height: 50px;
  width: 50px;
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 0 0.5rem;
}
.button-icon a {
  display: flex;
}
</style>
