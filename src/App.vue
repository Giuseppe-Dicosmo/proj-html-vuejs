<template>
  <div id="app">
    <headerWeb />
  </div>
</template>

<script>
import headerWeb from "./components/headerWeb.vue";

export default {
  name: "App",
  components: {
    headerWeb,
  },
};
</script>

<style lang="scss">
@import "./assets/scss/style.scss";

* {
  @include reset;
  // font-family: "bai-jamjuree", sans-serif;
}

#app {
  font-family: "bai-jamjuree", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
