<template>
  <div class="name_plate">
    <h1 class="color-white">Dylan Scherpf</h1>
    <h4 class="color-green">Front End Developer</h4>
    <div class="name_plate-links">
      <a href="https://github.com/dscherpf" target="_blank">
        <img src="../assets/github.svg" alt="Github logo" />
      </a>
      <a
        href="https://www.linkedin.com/in/dylan-scherpf-99499798/"
        target="_blank"
      >
        <img src="../assets/linkedin.svg" alt="LinkedIn logo" />
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'name-plate',
};
</script>

<style>
.name_plate-links {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}
.name_plate-links a {
  margin: 0 0.5rem;
}
</style>
