<template>
<div class="a-card">
    <div class="image-container"><img v-bind:src="image"/></div>
    <div class="content-container">
        <h3 class="project-title">{{projectName}}</h3>
        <p class="project-description">{{about}}</p>
    </div>
</div></template>

<script>
export default {
  name: "ProjectCard",
  props: {
    projectName: {
      type: String,
      default: "Project Definitely Defined In Code",
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
        default: "uhhhh"
    }
  },
};
</script>

<style scoped>

</style>