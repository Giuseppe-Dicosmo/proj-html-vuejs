<template>
  <section>
    <div class="container">
      <!-- ciclo card -->
      <div
        v-for="card in datiNav"
        :key="card.id"
        :class="card.class"
        class="wrapper"
      >
        <figure v-if="card.images">
          <img src="../assets/images/logotype-2-150x25.png" alt="" />
        </figure>

        <ul v-if="card.navFooter">
          <li v-for="(list, i) in card.navFooter" :key="i">
            <a v-if="list.link" :href="list.href">{{ list.link }}</a>

            <a v-if="list.linkIcons" :href="list.href">
              <img :src="list.linkIcons" alt="" />
            </a>
          </li>
        </ul>

        <p v-if="card.textCopyleft">{{ card.textCopyleft }}</p>
        <p v-if="card.textCopyright">{{ card.textCopyright }}</p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      datiNav: [
        {
          id: "1",
          class: "container-img",
          images: require(`../assets/images/logotype-2-150x25.png`),
        },
        {
          id: "2",
          class: "container-nav",
          navFooter: [
            {
              link: "home",
              href: "#",
            },
            {
              link: "about",
              href: "#",
            },
            {
              link: "projects",
              href: "#",
            },
            {
              link: "services",
              href: "#",
            },
            {
              link: "blog",
              href: "#",
            },
            {
              link: "contact",
              href: "#",
            },
          ],
        },
        {
          id: "3",
          class: "container-social",
          navFooter: [
            {
              linkIcons: require(`../assets/images/instagram.png`),
              href: "#",
            },
            {
              linkIcons: require(`../assets/images/linkedin.png`),
              href: "#",
            },
            {
              linkIcons: require(`../assets/images/facebook-app-symbol.png`),
              href: "#",
            },
            {
              linkIcons: require(`../assets/images/twitter.png`),
              href: "#",
            },
          ],
        },
        {
          id: "4",
          class: "container-copyright",
          textCopyleft: `Terms of use ${(<br />)} Privacy Environmental Policy`,
          textCopyright:
            "Copyright © 2020 Phlox Consulting. All Rights Reserved.",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
@import "../assets/scss/style.scss";

.container {
  @include container;
  height: 315px;
  display: flex;
  flex-flow: row wrap;

  .wrapper {
    width: calc(100% / 3);
    height: 60%;
    display: flex;
    flex-flow: row wrap;
    align-items: center;
    // border: 1px solid palegreen;

    ul {
      display: flex;
      gap: 30px;
      list-style: none;

      a {
        text-decoration: none;
      }
    }
  }

  .container-nav {
    justify-content: center;

    a {
      color: $grigio;
      text-transform: uppercase;
      @include font-size-15;

      &:hover {
        color: $rosso;
      }
    }
  }

  .container-social {
    justify-content: flex-end;

    li {
      width: 15px;
      aspect-ratio: auto 1 / 1;

      a img {
        width: 100%;
        height: 100%;
        object-fit: cover;

        &:hover {
          filter: invert(34%) sepia(97%) saturate(5277%) hue-rotate(339deg) brightness(94%) contrast(106%);
        }
      }
    }
  }

  .container-copyright {
    width: 100%;
    height: 40%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    position: relative;

    &::before {
      width: 100%;
      height: 1px;
      content: "";
      background: $indaco;
      position: absolute;
      top: 0;
    }

    p {
      color: $grigio;
    }
  }
}
</style>
