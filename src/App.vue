<template>
  <div class="main">
    <div class="header-container">
      <Header></Header>
    </div>
    <div class="content-container">
      <FancyName />
      <div class="card-container">
        
        <h2 id="about">About</h2>

        <About />

        <h2 id="projects">Projects</h2>
        <ProjectCard v-for="project in projects" :key="project"
          :projectName="project[0]"
          :link="project[1]"
          :about="project[2]"
          :image="project[3]"
        ></ProjectCard>

<h2 id="contact">Connect</h2>

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
import About from "./components/About.vue";


export default {
  name: "App",
  components: {
    Header,
    ProjectCard,
    FancyName,
    About
},
  data() {
    return {
      projects: [
        ["Brewery Bracket", "https://brewery-bracket-henryfaulkner.vercel.app/", "A bracket creator to facilitate a brewery-hopping weekend", image1],
        ["Hymnal Purchase Manager", "https://github.com/The-INTJ/pb-hymnals", "An E-commerce site facilitating the purchase of electronic hymnals", image2],
        ["Better Every Day", "https://github.com/The-INTJ/BetterEveryDayMERN", "A task tracker app to improve habits", image3],
        ["Boot Track", "https://github.com/The-INTJ/BootTrack-DT", "A mock-up MVC project that allowed a coding boot camp to track applicant progress", ],
      ]
    }
  }
};
</script>

<style lang="scss">
body {
  margin: 0;
  background-color: rgb(215, 215, 215);
}
h1 {
  font-size: 3em;
}
h2 {
  font-size: 2em;
  position: relative;
  &::before,
  &::after{
    content: "";
    display: inline-block;
    height: 1em;
    width: 5px;
    border: 1px solid lightgreen;
    position: absolute;
    background-color: lightgreen;
    transform: skew(-45deg, 0);
    left: -25px;
  }
  &::after {
    left: -40px;
  }
}
.main {
  display: flex;
  flex-direction: row;
  @media  (max-width: 1000px) {
    flex-direction: column;
  }
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
