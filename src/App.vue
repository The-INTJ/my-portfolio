<template>
  <div class="main">
    <div class="header-container">
      <Header></Header>
    </div>
    <div class="content-container">
      <FancyName />
      <div class="card-container">
        <ProjectCard />
        <ProjectCard />
        <ProjectCard />
        <ProjectCard />
        <ProjectCard />
        <ProjectCard />
      </div>
    </div>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import ProjectCard from "./components/ProjectCard.vue";
import FancyName from "./components/FancyName.vue";

export default {
  name: "App",
  components: {
    Header,
    ProjectCard,
    FancyName,
  },
};
</script>

<style>
body {
  margin: 0;
}
.main {
  display: flex;
  flex-direction: row;
}
.header-container {
  flex-grow: 1;
}
.content-container {
  flex-grow: 30;
}
.card-container {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  margin-top: 100px;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
