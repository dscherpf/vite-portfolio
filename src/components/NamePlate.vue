<template>
  <div class="name_plate">
    <h1 class="color-white">Dylan Scherpf</h1>
    <h2 class="color-green">Front End Developer</h2>
    <div class="name_plate-links">
      <ButtonIcon link="https://github.com/dscherpf" icon="github" />
      <ButtonIcon
        link="https://www.linkedin.com/in/dylan-scherpf-99499798/"
        icon="linkedin"
      />
    </div>
  </div>
</template>

<script>
import ButtonIcon from './ButtonIcon.vue';
export default {
  components: { ButtonIcon },
};
</script>

<style>
.name_plate {
  text-align: center;
  padding: 2rem;
}
.name_plate-links {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  margin-top: 2rem;
}
.name_plate-links a {
  margin: 0 0.5rem;
}
@media (min-width: 960px) {
  .name_plate {
    padding: 0;
    max-width: 310px;
    text-align: right;
  }
  .name_plate-links {
    justify-content: flex-end;
  }
}
</style>
