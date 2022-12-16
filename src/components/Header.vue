<template>
  <header>
    <div class="header-content">
      <a href="#projects">{{ projects }}</a>
      <a href="#about">{{ about }}</a>
      <a href="#contact">{{ contact}}</a>
      <a href="#surprise" class="the-surprise">{{ surpriseText }}</a>
    </div>
  </header>
</template>

<script>
export default {
  name: "v-header",
  props: {
    name: {
      type: String,
      default: "Me",
    },
    projects: {
      type: String,
      default: "Projects",
    },
    about: {
      type: String,
      default: "About",
    },
    contact: {
      type: String,
      default: "Contact"
    },
    surpriseText: {
      type: String,
      default: "You're approaching me?",
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../assets/styles/foundational/Header.scss';
</style>
