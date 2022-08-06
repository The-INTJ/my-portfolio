<template>
  <div class="a-card">
    <div class="blur-container"></div>
    <a :href="link">
      <img v-bind:src="image" />
    </a>
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
  background-color: lightgreen;

  transform: skew(-45deg, 0);

  * {
    transform: skew(45deg, 0);
  }
}
img {
  -webkit-transition: transform 0.5s ease-in-out;
    -moz-transition: transform 0.5s ease-in-out;
    transition: transform 0.5s ease-in-out;
}
img:hover {
 
    transform: skew(45deg, 0) scale(1.5);
    -webkit-transition: transform 0.5s ease-in-out;
    -moz-transition: transform 0.5s ease-in-out;
    transition: transform 0.5s ease-in-out;
}
img {
  width: 100%;
  position: absolute;
  left: 200px;
  transform: skew(-30deg, 0);
}
.content-container {
  position: absolute;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  align-items: flex-start;
  height: -webkit-fill-available;
  z-index: 2;
  right: 40%;
}
.blur-container {
  position: absolute;
  left: -250px;
  content: "";
  height: 100%;
  width: 100%;
  backdrop-filter: blur(10px);
  z-index: 1;
  transform: skew(0, 0);
}
.skew-cont {
  background-color: #141b29;
  color: white;
  border-radius: 10px;
  width: 270px;
  transform: skew(-45deg);
  > * {
    transform: skew(45deg);
  }

align-self: flex-end;

  &.alignment {
    margin-right: 85px;
    text-align: left;
  }
}
.project-title {
  margin: 10px 15px;
}
.project-description {
  margin: 10px 35px;
}
</style>