<template>
  <section class="container-fluid">
    <div class="container-empty"></div>
    <div class="container">
      <div class="container-description">
        <div class="container-description-empty"></div>
        <div class="wrapper">
          <div class="description">
            <span>about us</span>
            <h1>we make your strategy work</h1>
            <p>
              When, while lovely valley teems with vapour around meand eridian
              sun strikes the upper impenetrable foliage of my trees, and but a
              thousand unknown plants are noticed when I hear the buzz of the
              little world among the stalks,and grow familiar indescribable
              forms of the insects .and flies, then I feel the presence of the
              Almighty .
            </p>
          </div>
        </div>
      </div>
      <div class="business-case">
        <div class="card-business">
          <h3>we help to deliver the business case</h3>
          <p>
            When, while lovely valley teems with vapour around meand meridian
            sun strikes the upper impenetrable foliage of my trees, and but a
            thousand unknown
          </p>
        </div>
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
  background: url("../assets/images/business-people-working-together-on-project-and-5FHSKBL.jpg")
    no-repeat top left;
  background-size: 60% 840px;
  height: 1170px;
  position: relative;

  .container-empty {
    position: absolute;
    bottom: 0;
    width: 50%;
    height: 329px;
    border: 1px solid $verdeAcqua;
    background: $verdeAcqua;
  }
  .container {
    @include container;
    height: 100%;

    .container-description {
      width: 100%;
      height: 840px;
      // border: 1px solid yellow;
      display: flex;

      .container-description-empty {
        height: 100%;
        width: 60%;
        // border: 1px solid blueviolet;
      }
      .wrapper {
        height: 100%;
        width: 40%;
        // border: 3px solid darkgreen;
        display: flex;
        justify-content: center;
        align-items: center;

        .description {
          // border: 1px solid blueviolet;
          width: 80%;
          height: 50%;
          color: white;

          span {
            @include font-size-18;
            display: block;
            letter-spacing: 3px;
            text-transform: uppercase;
            color: $grigioAAAAAA;

            &::before {
              @include linea-text;
            }
          }

          h1 {
            font-size: 55px;
            margin: 45px 0;
            line-height: 50px;
            text-transform: uppercase;
          }

          p {
            @include font-size-18;
            line-height: 1.5em;
            color: $grigio;
          }
        }
      }
    }
    .business-case {
      background: $verdeAcqua;
      height: 329px;
      position: relative;
      display: flex;
      justify-content: center;
      align-items: center;

      .card-business {
        width: 85%;
        height: 85px;
        // border: 1px solid salmon;
        display: flex;
        gap: 360px;

        h3 {
          // border: 1px solid darkolivegreen;
          font-size: 30px;
          text-transform: uppercase;
          color: $violaScuro;
          width: 350px;
        }

        p {
          @include font-size-18;
          width: 600px;
          color: $violaScuro;
          font-weight: 100;
        }
      }

      button {
        position: absolute;
        bottom: 0;
        right: 0;
        width: 225px;
        height: 65px;
        background: $rosso;
        color: $white;
        @include font-size-18;
        text-transform: uppercase;
        cursor: pointer;
        border: none;

        &:hover {
          background: $violaScuro;
        }
      }
    }
  }
}
</style>
