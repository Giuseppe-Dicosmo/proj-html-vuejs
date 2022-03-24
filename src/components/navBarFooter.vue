<template>
  <section>
    <div class="container">
      <div class="container-img wrapper">
        <figure>
          <img src="../assets/images/logotype-2-150x25.png" alt="" />
        </figure>
      </div>
      <div class="container-nav wrapper">
        <ul>
          <li><a href="#">lorem</a></li>
          <li><a href="#">lorem</a></li>
          <li><a href="#">lorem</a></li>
          <li><a href="#">lorem</a></li>
          <li><a href="#">lorem</a></li>
          <li><a href="#">lorem</a></li>
        </ul>
      </div>
      <div class="container-social wrapper">
        <ul>
          <li>
            <a href="#">
              <img src="../assets/images/facebook-app-symbol.png" alt="" />
            </a>
          </li>
          <li>
            <a href="#">
              <img src="../assets/images/facebook-app-symbol.png" alt="" />
            </a>
          </li>
          <li>
            <a href="#">
              <img src="../assets/images/facebook-app-symbol.png" alt="" />
            </a>
          </li>
          <li>
            <a href="#">
              <img src="../assets/images/facebook-app-symbol.png" alt="" />
            </a>
          </li>
          <li>
            <a href="#">
              <img src="../assets/images/facebook-app-symbol.png" alt="" />
            </a>
          </li>
        </ul>
      </div>

      <div class="container-copyright">
        <p>
          Terms of use <br />
          Privacy Environmental Policy
        </p>

        <p>Copyright &#169; 2020 Phlox Consulting. All Rights Reserved.</p>
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
          images: require(`../assets/images/logotype-2-150x25.png`),
        },
        {
          id: "2",
          navFooter: [
            {
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
        },
        {
          id: "3",
          navIcons: [
            {
              icons: require(`../assets/images/instagram.png`),
              href: "#",
            },
            {
              icons: require(`../assets/images/linkedin.png`),
              href: "#",
            },
            {
              icons: require(`../assets/images/facebook-app-symbol.png`),
              href: "#",
            },
            {
              icons: require(`../assets/images/twitter.png`),
              href: "#",
            },
          ],
        },
        {
          id: "4",
          copyright: [
            {
              textCopyright: `Terms of use ${(
                <br />
              )} Privacy Environmental Policy`,
            },
            {
              textCopyright: "Copyright &#169; 2020 Phlox Consulting. All Rights Reserved.",
            },
          ],
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
    }
  }

  .container-social {
    justify-content: flex-end;

    li {
      width: 30px;
      aspect-ratio: auto 1 / 1;

      a img {
        width: 100%;
        height: 100%;
        object-fit: cover;
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
