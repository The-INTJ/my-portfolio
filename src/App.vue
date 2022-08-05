<template>
  <div class="main">
    <div class="header-container">
      <Header></Header>
    </div>
    <div class="content-container">
      <FancyName />
      <p class="short-desc">A passionate web developer who loves frameworks and styling</p>
      <div class="card-container">
        <h2 id="projects">Projects</h2>
        <ProjectCard v-for="project in projects" :key="project"
          :projectName="project[0]"
          :link="project[1]"
          :about="project[2]"
          :image="project[3]"
        ></ProjectCard>

        <h2 id="about">About</h2>

      </div>
    </div>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import ProjectCard from "./components/ProjectCard.vue";
import FancyName from "./components/FancyName.vue";
import image1 from "./assets/brewery.jpg";
import image2 from "./assets/pbhymnals2.jpg";
import image3 from "./assets/react.jpg";


export default {
  name: "App",
  components: {
    Header,
    ProjectCard,
    FancyName,
  },
  data() {
    return {
      projects: [
        ["Brewery Bracket", "https://brewery-bracket-henryfaulkner.vercel.app/", "desc", image1],
        ["Hymnal Purchase Manager", "d", "d", image2],
        ["Better Every Day", "d", "d", image3],
      ]
    }
  }
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
.short-desc {
  font-style: italic;
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
