<template>
  <nav>
    <figure>
      <img src="../assets/images/logotype.png" alt="" />
    </figure>
    <ul>
      <li class="active"><a href="#">lorem</a></li>
      <li><a href="#">lorem</a></li>
      <li><a href="#">lorem</a></li>
      <li><a href="#">lorem</a></li>
      <li><a href="#">lorem</a></li>
      <li><a href="#">lorem</a></li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: "navBar",


};
</script>

<style scoped lang="scss">
nav {
  width: 100%;
  border: 1px solid yellow;
  height: 75px;
  display: flex;
  align-items: center;
  background: transparent;
  position: sticky;
  top: 0;
  z-index: 1;
  gap: 38px;

  figure {
    height: 50%;
    // border: 1px solid fuchsia;
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
        color: #fff;
        font-size: 25px;
        text-decoration: none;
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
          background: #fff;
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
