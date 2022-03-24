<template>
  <section class="container-fluid">
    <div class="container">
      <div class="container-blog">
        <!-- Sezione titolo -->
        <div class="wrapper">
          <div class="title">
            <span>blog</span>
            <h1>the recent news you must read it</h1>
          </div>
          <button class="container-arrows">view all</button>
        </div>

        <!-- Sezione Notizie -->
        <div class="container-news">
          <div v-for="(card, i) in datiCard" :key="i" class="news-card">
            <figure>
              <img :src="card.images" alt="" />
            </figure>
            <div class="container-info-news">
              <div class="info-news">
                <div class="published">
                  <a :href="card.href">{{ card.data }}</a>
                  <a :href="card.href">by {{ card.name }}</a>
                </div>
                <h3>{{ card.titol }}</h3>
                <p>{{ card.text }}</p>
              </div>
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
          images: require(`../assets/images/startup-business-people-and-strategy-board-PAJ3P9K-1390x1042.jpg`),
          data: "july 4, 2019",
          name: "paul",
          href: "#",
          titol: "Canadian Consulting Firm acquired by UK Giant",
          text: "When, while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a ...",
        },
        {
          images: require(`../assets/images/business-people-working-together-on-project-and-5FHSKBL-1390.jpg`),
          data: "july 4, 2019",
          name: "paul",
          href: "#",
          titol: "Canadian Consulting Firm acquired by UK Giant",
          text: "When, while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a ...",
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
    height: 1350px;
    display: flex;
    align-items: center;

    .container-blog {
      width: 100%;
      height: 760px;

      .wrapper {
        height: 200px;
        display: flex;
        align-items: center;
        justify-content: space-between;

        .title {
          width: 70%;
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

        button {
          @include botton;
          @include font-size-18;
          border: none;
          background: $verdeAcqua;
          color: $violaScuro;

          &:hover {
            background: $rosso;
            color: $white;
          }
        }
      }

      // Sezione Notizie
      .container-news {
        width: 100%;
        height: 560px;
        display: flex;
        gap: 30px;
        .news-card {
          width: calc(100% / 2);
          height: 100%;
          position: relative;
          figure {
            height: 100%;
            overflow: hidden;

            img {
              transition: all 0.6s ease-in-out;
              width: 100%;
              height: 100%;
              object-fit: cover;
            }
          }

          &:hover {
            img {
              transform: scale(1.1);
            }
            .container-info-news {
              background: $verdeAcqua;
              transform: translate(0, 40%);
            }
          }

          .container-info-news {
            transition: transform 0.6s ease-in-out;
            width: 80%;
            height: 60%;
            background: $white;
            position: absolute;
            display: flex;
            justify-content: center;
            align-items: center;
            bottom: 0;
            right: 0;
            transform: translate(0, 35%);

            .info-news {
              width: 70%;
              height: 70%;
              // border: 1px solid blue;
              display: flex;
              flex-direction: column;
              justify-content: space-evenly;

              .published {
                display: flex;
                gap: 20px;

                a {
                  color: $rosso;
                  text-decoration: none;
                  @include font-size-15;
                }
              }

              h3 {
                font-size: 27px;
              }

              p {
                @include font-size-15;
              }
            }
          }
        }
      }
    }
  }
}
</style>
