<template>
  <header class="container-fluid">
    <div class="container">
      <navBar />
      <JumboTron />
    </div>
      <div class="background-img" ></div>
  </header>
</template>

<script>
import navBar from "./navBar.vue";
import JumboTron from "./JumboTron.vue";


export default {
  name: "headerWeb",
  components: {
    navBar,
    JumboTron
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../assets/scss/style.scss";


.container-fluid {
  background: url("../assets/images/portrait-of-young-architect-woman-on-meeting-KFZCE3A.jpg") no-repeat right;
  background-size: 65% 100%;

  .container {
    @include container;
    height: 992px;
  }
}
</style>
