<template>
  <div class="container-jumbotron">
    <div class="description">
      <p>alwats the best way you need it</p>
      <h1>the best business consulting</h1>
      <div class="container-play">
        <button>read more</button>
        <figure class="play">
          <a href="#">
            <img src="../assets/images/play.png" alt="" />
          </a>
        </figure>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped lang="scss">
@import "../assets/scss/style.scss";

.container-jumbotron {
  width: 100%;
  height: calc(992px - 75px);
  display: flex;
  position: relative;
  // border: 1px solid yellow;
  display: flex;
  align-items: center;

  .description {
    width: 45%;
    height: 50%;
    // border: 1px solid fuchsia;
    color: $white;
    text-transform: uppercase;

    p {
      @include font-size-15;
      display: block;
      letter-spacing: 3px;
    }

    p::before {
      display: inline-block;
      width: 55px;
      height: 5px;
      margin-right: 20px;
      content: "";
      background: $verdeAcqua;
      border-radius: 5px;
    }

    h1 {
      font-size: 105px;
      margin: 45px 0;
      line-height: 90px;
    }

    .container-play {
      display: flex;
      align-items: center;
      gap: 35px;

      button {
        width: 232px;
        height: 70px;
        background: $verdeAcqua;
        border: none;
        @include font-size-15;
        text-transform: uppercase;

        &:hover{
          background: $rosso;
          color: $white;
        }
      }


      .play {
        width: 60px;
        height: 60px;
        border: 2px solid $white;
        border-radius: 50%;
        display: flex;
        align-items: center;
        justify-content: center;


        a {
          width: 16px;
          height: 16px;
          img {
            max-width: 100%;
          }
        }
      }
    }
  }
}
</style>
