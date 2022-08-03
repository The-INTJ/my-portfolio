<template>
    <div class="name-container">
      <h1 class="the-surprise">{{ name }}</h1>
    </div>
</template>

<script>
export default {
  name: "fancyName",
  props: {
    name: {
      type: String,
      default: "Drew Taylor",
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>

