<template>
  <div id="app">
    <headerWeb />
    <mainWeb />
    <footerWeb />
  </div>
</template>

<script>
import headerWeb from "./components/headerWeb.vue";
import mainWeb from "./components/mainWeb.vue";
import footerWeb from "./components/footerWeb.vue";

export default {
  name: "App",
  components: {
    headerWeb,
    mainWeb,
    footerWeb,
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
