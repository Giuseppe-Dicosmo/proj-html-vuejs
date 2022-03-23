<template>
  <section class="container-fluid">
    <div class="container"></div>
    <div class="container-empty"></div>
  </section>
</template>

<script>
export default {};
</script>

<style scoped lang="scss">
@import "../assets/scss/style.scss";

.container-fluid {
  // background: salmon;
  height: 570px;
  position: relative;

  .container-empty {
    position: absolute;
    right: 0;
    bottom: 0;
    width: 50%;
    height: 365px;
    background: $white;
  }
}
</style>
