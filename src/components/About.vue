<template>
  <div class="about-container">
    <p class="intro">
      A passionate front end developer with a love for styling, frameworks, and
      people. If he's not applying questionable style choices to the newest
      anotherone.js site he built, then he's probably rock climbing.
    </p>
    <div class="section-container">
      <div class="sub-section">
        <h4>Professional Experience</h4>
        <p class="banner-text">Perficient</p>
        <p class="description">
          Drew is an Associate Technical Consultant at Perficient, where he has
          worked as a developer on multiple SXA sites. In this role, he has
          gained experience leading deploys, operating and monitoring production
          resources, and overseeing the codebase. He has also built components
          from scratch and architected style and accessibility efforts.
        </p>
        <p class="description">
          Drew is skilled in a range of technologies, including languages such
          as JavaScript, Typescript, JSX, HTML, CSS, and SASS, as well as
          frameworks like Next.js, ASP.NET, and libraries such as jQuery,
          React.js, and SXA. He has experience with content management systems
          like Sitecore and cloud deployment platforms like Azure and Vercel.
        </p>
        <p class="description">
          In addition to these technologies, Drew is proficient in Git Bash,
          Linux, Solr, Azure DevOps, and Visual Studio.Drew works as Technical
          Consultant, specializing in front end frameworks, WACG, and enjoys
          learning the best high-level approaches for organizing code. He has
          worked with a variety of team sizes and delivered work for
          enterprise-scale Websites.
        </p>
      </div>
      <div class="sub-section">
        <h4>Education</h4>
        <p class="banner-text">University of Georgia</p>
        <p class="description">
          Drew attended the University of Georgia, where he led the Computer
          Science Interview Prep Club, and graduated Cum Laude.
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "about-me",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
p {
  font-size: large;
  text-align: left;
}
h4 {
  font-size: larger;
}
.about-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 80%;
}

.section-container {
  display: flex;
  flex-direction: column;
  justify-content: space-around;
}

.intro {
  font-style: italic;
  margin: 0 0 35px 0;
  text-align: center;
}

.sub-section {
  padding: 10px;
  border-radius: 10px;
  display: flex;
  flex-direction: column;
  align-items: baseline;
}

.banner-text {
  font-weight: bold;
  font-style: italic;
}
</style>

