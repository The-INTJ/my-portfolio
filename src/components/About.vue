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
          Drew works as Technical Consultant, specializing in front end
          frameworks, WACG, and enjoys learning the best high-level approaches
          for organizing code. He has worked with a variety of team sizes and
          delivered work for enterprise-scale Websites.
        </p>
        <p class="description">
          His current roles have worked with React, JavaScript, SASS/SCSS, C#,
          and involved management and deployment through Azure.
        </p>
      </div>
      <div class="sub-section">
        <h4>Education</h4>
        <p class="banner-text">University of Georgia</p>
        <p class="description">
          Drew works as Technical Consultant, specializing in front end
          frameworks, WACG, and enjoys learning the best high-level approaches
          for organizing code. He has worked with a variety of team sizes and
          delivered work for enterprise-scale Websites.
        </p>
        <p class="description">
          His current roles have worked with React, JavaScript, SASS/SCSS, C#,
          and involved management and deployment through Azure.
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

