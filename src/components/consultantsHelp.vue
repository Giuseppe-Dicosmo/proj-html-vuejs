<template>
  <section class="container-fluid">
    <div class="container">
      <div class="container-consultants">
        <h2>our consultants can help you</h2>
        <ul class="container-card">
          <li v-for="(card, i) in datiCard" :key="i" class="card">
            <figure class="img-card">
              <img :src="card.images" alt="" />
            </figure>
            <div class="container-text-card">
              <h3>{{ card.titol }}</h3>
              <p>{{ card.text }}</p>
            </div>
          </li>
        </ul>
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
          images: require(`../assets/images/stats.png`),
          titol: "statistical consulting",
          text: "When, while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a",
        },
        {
          images: require(`../assets/images/promotion.png`),
          titol: "digital consulting",
          text: "When, while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a",
        },
        {
          images: require(`../assets/images/wallet.png`),
          titol: "banking consulting",
          text: "When, while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a",
        },
        {
          images: require(`../assets/images/target.png`),
          titol: "enterprise consulting",
          text: "When, while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
@import "../assets/scss/style.scss";

.container-fluid {
  background: $white;

  .container {
    @include container;
    height: 890px;
    display: flex;
    align-items: center;
    justify-content: center;

    .container-consultants {
      width: 85%;
      height: 70%;
      display: flex;
      flex-direction: column;
      justify-content: space-between;

      h2 {
        font-size: 30px;
        text-transform: uppercase;
        position: relative;

        &::after {
          display: inline-block;
          width: 100vw;
          height: 5px;
          content: "";
          background: $verdeAcqua;
          border-radius: 5px;
          margin-left: 40px;
          position: absolute;
          top: 50%;
          transform: translate(0, -50%);
        }
      }

      .container-card {
        width: 100%;
        height: 445px;
        display: flex;
        flex-wrap: wrap;
        gap: 125px 250px;

        .card {
          width: calc((100% / 2) - 125px);
          // border: 2px solid red;
          display: flex;

          .img-card {
            border: 1px solid $rosso;
            background: $rosso;
            border-radius: 50%;
            width: 70px;
            height: 70px;
            flex-shrink: 0;
            margin-right: 45px;
            display: flex;
            justify-content: center;
            align-items: center;

            img {
              max-width: 60%;
            }
          }
          .container-text-card {
            h3 {
              line-height: 2.5em;
              text-transform: uppercase;
              font-size: 25px;
            }

            p {
              @include font-size-18;
              color: $grigio;
            }
          }
        }
      }
    }
  }
}
</style>
