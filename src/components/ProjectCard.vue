<template>
  <div class="a-card">
    <div class="blur-container"></div>
    <img v-bind:src="image" />
    <div class="content-container">
      <div class="skew-cont">
        <h3 class="project-title">{{ projectName }}</h3>
      </div>
      <div class="skew-cont alignment">
        <p class="project-description">{{ about }}</p>
      </div>
    </div>
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
      default: require("../assets/codeImage.jpeg"),
    },
  },
};
</script>
<style scoped lang="scss">
.a-card {
  height: 200px;
  width: 600px;
  overflow: hidden;
  border-radius: 10px;
  margin: 25px;

  transform: skew(45deg, 0);

  > * {
    transform: skew(-45deg, 0);
  }
}
img {
  width: 160%;
  height: 160%;
  position: absolute;
  left: -265px;
  transform: skew(30deg, 0);
}
.content-container {
  position: absolute;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  align-items: flex-start;
  height: -webkit-fill-available;
  z-index: 2;
}
.blur-container {
  position: absolute;
  left: -250px;
  content: "";
  height: 100%;
  width: 100%;
  backdrop-filter: blur(10px);
  z-index: 1;
}
.skew-cont {
  background-color: #141b29;
  color: white;
  border-radius: 10px;
  transform: skew(45deg);
  > * {
    transform: skew(-45deg);
  }

  &.alignment {
    margin-left: 85px;
  }
}
.project-title {
  margin: 10px 15px;
}
.project-description {
  margin: 10px 15px;
  max-width: 200px;
}
</style>