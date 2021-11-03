<template>
  <div class="name_plate">
    <h1 class="color-white">Dylan Scherpf</h1>
    <h4 class="color-green">Front End Developer</h4>
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
  max-width: 300px;
  text-align: right;
}
.name_plate-links {
  display: flex;
  flex-direction: row;
  justify-content: flex-end;
  align-items: center;
  margin-top: 2rem;
}
.name_plate-links a {
  margin: 0 0.5rem;
}
</style>
