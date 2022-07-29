<template>
  <header>
    <div class="spacer"></div>
    <div class="header-content">
      <p>{{ projects }}</p>
      <p>{{ about }}</p>
      <p class="the-surprise">{{ surpriseText }}</p>
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
  p {
    padding: 15px;
  }
}
.spacer {
  height: 20vh;
  visibility: hidden;
}
.header-content{
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  align-items: center;
  height: 60vh;
  background-color: #141b29;
  color: white;
  border-top-right-radius: 10px;
  border-bottom-right-radius: 10px;
}
</style>
