<template>
  <section class="container-fluid">
    <div class="container">
      <div class="wrapper">
        <h3>let's talk about work</h3>
        <p>
          A wonderful serenity has taken possession Far far away, behind the
          word mountains.
        </p>
        <button>get started</button>
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style scoped lang="scss">
@import "../assets/scss/style.scss";

.container-fluid {
  background: url("../assets/images/business-people-working-together-on-project-and-B3MZ4TX.jpg")
    no-repeat center;
  background-size: cover;

  .container {
    height: 457px;
    display: flex;
    justify-content: center;
    align-items: center;

    .wrapper {
      width: 700px;
      height: 200px;
      display: flex;
      flex-direction: column;
      justify-content: space-around;
      align-items: center;

      h3,
      p, button {
        text-align: center;
        color: $white;
      }

      h3 {
        font-size: 40px;
        text-transform: uppercase;
      }

      p {
        @include font-size-18;
      }

      button {
        background: $violaScuro;
        border: none;
        @include botton;
        @include font-size-18;
      }

      button:hover {
        background: $verdeAcqua;
        color: $violaScuro;
      }
    }
  }
}
</style>
