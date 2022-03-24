<template>
  <section class="container-fluid">
    <div class="container">
      <div class="container-project">
        <!-- Sezione titolo -->
        <div class="wrapper">
          <div class="title">
            <span>project</span>
            <h1>our expert trusted consultants help clients</h1>
          </div>
          <div class="container-arrows">
            <div class="arrows">&#8592;</div>

            <div class="arrows">&#8594;</div>
          </div>
        </div>
        <!-- Sezione card -->
        <div class="container-slide">
          <div v-for="(card, i) in datiCard" :key="i" class="slide">
            <figure>
              <img :src="card.images" alt="" />
            </figure>
            <div class="info-hover">
              <div class="info">
                <h3>{{ card.titol }}</h3>
                <span>{{ card.text }}</span>
              </div>

              <div class="botton-icon">&#43;</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      datiCard: [
        {
          images: require(`../assets/images/DRY-1-790x592.jpg`),
          titol: "purinky products",
          text: "uncategorized",
        },
        {
          images: require(`../assets/images/221bf0b7-8134-43bb-936a-5acbe42db64a-790x592.jpg`),
          titol: "purinky products",
          text: "uncategorized",
        },
        {
          images: require(`../assets/images/z1el4c4p-790x592.jpg`),
          titol: "purinky products",
          text: "uncategorized",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
@import "../assets/scss/style.scss";

.container-fluid {
  .container {
    @include container;
    height: 970px;
    display: flex;
    align-items: center;

    .container-project {
      width: 100%;
      height: 590px;
      // border: 1px solid darkgreen;

      .wrapper {
        // border: 1px solid blue;
        height: 200px;
        display: flex;
        align-items: center;
        justify-content: space-between;

        .title {
          width: 45%;
          // border: 1px solid greenyellow;
          height: 100%;
          display: flex;
          flex-direction: column;
          justify-content: space-between;

          span {
            @include font-size-18;
            @include text-top-title;

            &::before {
              @include linea-text;
            }
          }

          h1 {
            font-size: 48px;
            color: $white;
            height: 100%;
            display: flex;
            align-items: center;
            text-transform: uppercase;
          }
        }

        .container-arrows {
          display: flex;
          gap: 10px;

          .arrows {
            @include botton-icons;

            &:hover {
              background: $verdeAcqua;
            }
          }
        }
      }

      .container-slide {
        height: 390px;
        // border: 1px solid yellow;
        display: flex;
        gap: 30px;

        .slide {
          width: calc(100% / 3);
          position: relative;
          overflow: hidden;
          // border: 2px solid rgb(255, 0, 128);

          figure {
            height: 100%;
            // border: 2px solid rgb(0, 38, 255);

            img {
              transition: all 0.5s ease-in-out;
              max-width: 100%;
              object-fit: cover;
            }
          }

          .info-hover {
            transition: all 0.5s ease-in-out;
          }

          &:hover {
            figure {
              img {
                transform: scale(1.2);
              }
            }

            .info-hover {
              background: rgba(248, 29, 57, 0.7);
              // mix-blend-mode: multiply;
              padding: 30px;
              display: flex;
              flex-wrap: wrap;
              justify-content: space-between;
              align-items: center;
              align-content: flex-end;
              position: absolute;
              inset: 0;
              // top: 0;
              // left: 0;
              // bottom: 0;
              // right: 0;

              .info {
                h3 {
                  font-size: 25px;
                  color: $white;
                  line-height: 35px;
                  text-transform: capitalize;
                }

                span {
                  color: $grigio;
                }
              }

              .botton-icon {
                @include botton-icons;
                // @include font-size-18;
                font-size: 30px;

                &:hover {
                  background: $verdeAcqua;
                }
              }
            }
          }
        }
      }
    }
  }
}
</style>
