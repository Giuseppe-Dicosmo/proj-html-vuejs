<template>
  <header class="container-fuil">
    <div class="container">
      <navBar />
    </div>
  </header>
</template>

<script>
import navBar from "./navBar.vue";

export default {
  name: "headerWeb",
  components: {
    navBar,
  }
  // props: {
  //   msg: String
  // }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../assets/scss/style.scss";

$violaScuro: #1f1e38;

.container-fuil {
  background: $violaScuro;
  width: 100%;

  .container {
    @include container;
    height: 992px;
  }
}
</style>
