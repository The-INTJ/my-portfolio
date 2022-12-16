<template>
  <div class="main">
    <v-header />
    <div class="content-container">
      <FancyName />
      <div class="card-container">
        <h2 id="about">About</h2>

        <About />

        <h2 id="projects">Projects</h2>
        <project-card
          v-for="project in projects"
          :key="project"
          :projectName="project[0]"
          :link="project[1]"
          :about="project[2]"
          :image="project[3]"
        />

        <h2 id="contact">Connect</h2>
        <v-connect />
      </div>
    </div>
  </div>
</template>

<script>
import vHeader from "./components/Header.vue";
import ProjectCard from "./components/ProjectCard.vue";
import FancyName from "./components/FancyName.vue";
import image1 from "./assets/brewery.jpg";
import image2 from "./assets/pbhymnals2.jpg";
import About from "./components/About.vue";
import vConnect from "./components/Connect.vue";

export default {
  name: "App",
  components: {
    vHeader,
    ProjectCard,
    FancyName,
    About,
    vConnect,
  },
  data() {
    return {
      projects: [
        [
          "Brewery Bracket",
          "https://brewery-bracket-henryfaulkner.vercel.app/",
          "A bracket creator to facilitate a brewery-hopping weekend",
          image1,
        ],
        [
          "Hymnal Purchase Manager",
          "https://github.com/The-INTJ/pb-hymnals",
          "An E-commerce site facilitating the purchase of electronic hymnals",
          image2,
        ],
        [
          "Better Every Day",
          "https://github.com/The-INTJ/BetterEveryDayMERN",
          "A task tracker app to improve habits",
        ],
        [
          "Boot Track",
          "https://github.com/The-INTJ/BootTrack-DT",
          "A mock-up MVC project that allowed a coding boot camp to track applicant progress",
        ],
      ],
    };
  },
};
</script>

<style lang="scss">
@import "./assets/styles/components/app.scss";
</style>
