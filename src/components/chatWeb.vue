<template>
  <div class="container-button">
    <button class="top-page" @click="topPage()">
      <img src="../assets/images/arrow_up_icon_128384.svg" alt="" />
    </button>
    <button class="chat">
      <img src="../assets/images/chatspeechballoon_85812.svg" alt="" />
    </button>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  methods: {
    topPage: function () {
      window.scrollTo({ top: 0, behavior: "smooth" });
    },
  },
};
</script>

<style scoped lang="scss">
@import "../assets/scss/style.scss";

.container-button {
  width: 120px;
  height: 70px;
  position: fixed;
  bottom: 40px;
  right: 40px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  z-index: 2;

  .top-page {
    width: 25%;
    aspect-ratio: 1 / 1;
    border-radius: 50%;
    border: 1px solid $grigio;
    background: $white;
    cursor: pointer;
    translate: all 3s;
    color: $grigio;

    img {
      width: 50%;
      aspect-ratio: 1 / 1;
    }

    &:hover {
      transition: all 0.5s ease-in-out;
      background: #3d3d3d;
      border: 1px solid $white;

      img {
        filter: invert(98%) sepia(0%) saturate(7483%) hue-rotate(39deg) brightness(105%) contrast(100%);
      }
    }
  }

  .chat {
    width: 50%;
    aspect-ratio: 1 / 1;
    border-radius: 50%;
    border: none;
    cursor: pointer;
    background: #527ceb;

    img {
      width: 50%;
      aspect-ratio: 1 / 1;
      filter: invert(98%) sepia(0%) saturate(7483%) hue-rotate(39deg) brightness(105%) contrast(100%);
    }

    &:hover {
      background: #466dd6;
    }
  }
}
</style>
