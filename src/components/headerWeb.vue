<template>
  <header class="container-fuil">
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
  // props: {
  //   msg: String
  // }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../assets/scss/style.scss";


.container-fuil {
  background: $violaScuro url("../assets/images/portrait-of-young-architect-woman-on-meeting-KFZCE3A.jpg") no-repeat right;
  background-size: contain 65% 100%;
  width: 100%;

  .container {
    @include container;
    height: 992px;
  }
}
</style>
