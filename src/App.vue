<template>
  <div class="main">
    <div class="header-container">
      <Header></Header>
    </div>
    <div class="content-container">
      <h1>thing</h1>
      <h1>thing</h1>
      <h1>thing</h1>
      <h1>thing</h1>
      <h1>thing</h1>
      <h1>thing</h1>
      <h1>thing</h1>
      <h1>thing</h1>
      <h1>thing</h1>
      <h1>thing</h1>
      <h1>thing</h1>
      <h1>thing</h1>
      <h1>thing</h1>
      <h1>thing</h1>
      <h1>thing</h1>
      <h1>thing</h1>
      <h1>thing</h1>
      <h1>thing</h1>
      <h1>thing</h1>
      <h1>thing</h1>
      <h1>thing</h1>
      <h1>thing</h1>
    </div>
  </div>
</template>

<script>
import Header from "./components/Header.vue";

export default {
  name: "App",
  components: {
    Header,
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
  flex-grow: 9;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
