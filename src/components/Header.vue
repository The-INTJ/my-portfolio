<template>
  <header>
    <div class="spacer"></div>
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
  name: "customHeader",
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
header {
  position: sticky;
  top: 0;
  min-width: 200px;
  a {
    color: white;
    padding: 15px;
    font-weight: bolder;
    font-size: 1.2em;
    text-decoration: none;
    &:hover {
      color: lightgreen;
    }
  }
}
.the-surprise {
  visibility: hidden;
  position: absolute;
}
.spacer {
  height: 20vh;
  visibility: hidden;
}
.header-content {
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  align-items: center;
  height: 60vh;
  background-color: #141b29;
  color: white;
  border-top-right-radius: 10px;
  border-bottom-right-radius: 10px;
  box-shadow: 0 0 30px 1px #141b29;
}
</style>
