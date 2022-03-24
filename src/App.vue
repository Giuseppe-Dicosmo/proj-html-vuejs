<template>
  <div id="app">
    <headerWeb />
    <mainWeb />
    <footerWeb />
    <chatWeb />
  </div>
</template>

<script>
import headerWeb from "./components/headerWeb.vue";
import mainWeb from "./components/mainWeb.vue";
import footerWeb from "./components/footerWeb.vue";
import chatWeb from "./components/chatWeb.vue";

export default {
  name: "App",
  components: {
    headerWeb,
    mainWeb,
    footerWeb,
    chatWeb,
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
  overflow-x: hidden;
  background: $violaScuro;
}
</style>
