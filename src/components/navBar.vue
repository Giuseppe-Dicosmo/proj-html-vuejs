<template>
  <nav>
    <figure>
      <img :src="require(`../assets/images/${imgLogo}`)" alt="" />
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
  position: sticky;
  top: 0;
  z-index: 1;
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

        a {
          color: rgba($color: $white, $alpha: 1);
          font-weight: bold;
        }
      }
    }
  }
}
</style>
