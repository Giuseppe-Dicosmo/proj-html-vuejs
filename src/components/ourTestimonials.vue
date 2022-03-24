<template>
  <section class="container-fluid">
    <div class="container">
      <div class="title">
        <span>testimonial</span>
        <h1>what's the customer say about our work</h1>
      </div>
      <div class="container-card">
        <div v-for="(card, i) in datiCard" :key="i" class="card">
          <figure>
            <img :src="card.images" alt="" />
          </figure>

          <div class="wrapper">
            <p class="description">{{ card.text }}</p>

            <div class="person">
              <h3>{{ card.titol }}</h3>
              <div class="agency">{{ card.agency }}</div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="container-empty"></div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      datiCard: [
        {
          images: require(`../assets/images/oliver-ragfelt-488196-2.jpg`),
          text: "When, while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a thousand unknown plants are noticed by when I hear the buzz of the little.",
          titol: "Vera Duncan",
          agency: "Amazon Inc",
        },
        {
          images: require(`../assets/images/12679.jpg`),
          text: "When, while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a thousand unknown plants are noticed by when I hear the buzz of the little.",
          titol: "Vera Duncan",
          agency: "Amazon Inc",
        },
        {
          images: require(`../assets/images/oliver-ragfelt-488196-unsplash.jpg`),
          text: "When, while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a thousand unknown plants are noticed by when I hear the buzz of the little.",
          titol: "Vera Duncan",
          agency: "Amazon Inc",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
@import "../assets/scss/style.scss";

.container-fluid {
  // background: salmon;
  height: 570px;
  position: relative;

  .container {
    @include container;
    height: 100%;

    .title {
      height: 205px;
      // border: 1px solid salmon;
      display: flex;
      flex-direction: column;
      align-items: flex-end;

      span {
        @include font-size-18;
        @include text-top-title;
        width: 100%;
        // border: 1px solid antiquewhite;
        text-align: center;

        &::before {
          @include linea-text;
          position: absolute;
          right: 0;
          bottom: 5px;
        }
      }

      h1 {
        width: 50%;
        height: 100%;
        font-size: 48px;
        text-transform: uppercase;
        text-align: end;
        color: $white;
        display: flex;
        align-items: center;
        // border: 1px solid yellow;
      }
    }

    .container-card {
      // width: 100%;
      height: 365px;
      background: $white;
      display: flex;

      .card {
        width: calc(100% / 3);
        height: 100%;
        // border: 1px solid salmon;
        position: relative;
        display: flex;
        justify-content: center;
        align-items: center;
        z-index: 1;

        figure {
          width: 100%;
          height: 100%;

          img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            opacity: 0;
          }
        }

        &:hover img {
          transition: all 0.4s ease-in-out;
          opacity: 1;
        }

        &:hover h3 {
          transition: all 0.4s ease-in-out;
          color: $white;
        }

        .wrapper {
          width: 70%;
          height: 70%;
          // border: 3px solid salmon;
          position: absolute;
          display: flex;
          flex-direction: column;
          justify-content: space-around;

          .description {
            @include font-size-18;
            color: $grigio;
          }

          .person {
            h3 {
              font-size: 24px;
            }
            .agency {
              @include font-size-18;
              color: $grigio;
            }
          }
        }
      }
    }
  }
  .container-empty {
    position: absolute;
    bottom: 0;
    right: 0;
    width: 50%;
    height: 365px;
    background: $white;
  }
}
</style>
