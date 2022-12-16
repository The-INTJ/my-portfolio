<template>
  <div class="a-card">
    <div class="blur-container"></div>
    <div class="content-container">
      <div class="skew-cont">
        <a class="text" :href="link"><h3 class="project-title">{{ projectName }}</h3></a>
      </div>
      <div class="skew-cont alignment">
        <a class="text align" :href="link"><p class="project-description">{{ about }}</p></a>
      </div>
    </div>
    <a :href="link" tabindex="-1">
      <img v-bind:src="image" />
    </a>
  </div>
</template>

<script>
export default {
  name: "ProjectCard",
  props: {
    projectName: {
      type: String,
      default: "Project Alpha",
    },
    link: {
      type: String,
      default: "https://github.com/The-INTJ",
    },
    about: {
      type: String,
      default: "This is one of the projects of all time",
    },
    image: {
      type: String,
      default: require("../assets/coding2.jpg"),
    },
  },
};
</script>
<style scoped lang="scss">
@import "../assets/styles/components/ProjectCard.scss";
</style>