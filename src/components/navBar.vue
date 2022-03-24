<template>
  <nav>
    <figure>
      <a href="https://demo.phlox.pro/consulting-2/">
        <img :src="require(`../assets/images/${imgLogo}`)" alt="" />
      </a>
    </figure>
    <ul>
      <li
        :class="link.active ? 'active' : ''"
        v-for="(link, i) in datiNav"
        :key="i"
      >
        <a :href="link.href">
          {{ link.text }}
        </a>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: "navBar",
  data() {
    return {
      imgLogo: "logotype.png",
      datiNav: [
        {
          active: "true",
          text: "home",
          href: "#",
        },
        {
          text: "about",
          href: "#",
        },
        {
          text: "projects",
          href: "#",
        },
        {
          text: "services",
          href: "#",
        },
        {
          text: "blog",
          href: "#",
        },
        {
          text: "contact",
          href: "#",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
@import "../assets/scss/style.scss";

nav {
  width: 100%;
  height: 75px;
  display: flex;
  align-items: center;
  gap: 38px;

  figure {
    height: 20px;
    flex-grow: 1;
    img {
      max-height: 100%;
    }
  }

  ul {
    display: contents;
    list-style: none;

    li {
      height: 100%;
      display: flex;
      align-items: center;

      a {
        color: rgba($color: $white, $alpha: 0.5);
        @include font-size-15;
        text-decoration: none;
        text-transform: uppercase;
        position: relative;
        display: block;
        height: 100%;
        display: flex;
        align-items: center;
        // border: 1px solid darkolivegreen;

        &::before {
          transition: all 0.3s linear;
          display: block;
          width: 0;
          height: 5px;
          content: "";
          background: $white;
          border-radius: 5px;
        }
      }

      &.active {
        a {
          color: rgba($color: $white, $alpha: 1);
          font-weight: bold;
        }
      }

      &.active,
      &:hover {
        a::before {
          display: block;
          width: 100%;
          height: 5px;
          content: "";
          background: $white;
          border-radius: 5px;
          position: absolute;
          top: 0;
          left: 0;
          right: 0;
        }
      }
    }
  }
}
</style>
