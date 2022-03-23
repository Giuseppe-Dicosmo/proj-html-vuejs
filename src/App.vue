<template>
  <div id="app">
    <headerWeb />
    <mainWeb />
  </div>
</template>

<script>
import headerWeb from "./components/headerWeb.vue";
import mainWeb from "./components/mainWeb.vue";

export default {
  name: "App",
  components: {
    headerWeb,
    mainWeb
  },
};
</script>

<style lang="scss">
@import "./assets/scss/style.scss";

* {
  @include reset;
}

#app {
  font-family: "bai-jamjuree", sans-serif;
  // -webkit-font-smoothing: antialiased;
  // -moz-osx-font-smoothing: grayscale;
  overflow-x: hidden;
  background: $violaScuro;
}
</style>
