<template>
  <div class="wrapper-nav">
    <NavDesktop class="nav-desktop" />
    <div class="home-wrapper">
      <div class="text-wrapper">
        <p class="hello">Hello!</p>
        <p class="iam">I'm Lola Rufino</p>
        <p class="profession">Fullstack Developer & Photographer</p>
        <div class="icons-wrapper">
          <a
            href="https://www.linkedin.com/in/lola-rufino/"
            target="_blank"
            rel="noopener"
            ><img
              class="icon"
              src="https://i.ibb.co/ZYTF7mc/linkedin-2-pink.png"
              alt="Linkedin icon"
          /></a>
          <a href="https://github.com/lolarufino" target="_blank" rel="noopener"
            ><img
              class="icon"
              src="https://i.ibb.co/5KrcTBM/github-1-pink.png"
              alt="Github icon"
          /></a>
          <a
            href="https://twitter.com/lolarufino"
            target="_blank"
            rel="noopener"
            ><img
              class="icon"
              src="https://i.ibb.co/HNT8DJx/gorjeopink.png"
              alt="Twitter icon"
          /></a>
        </div>
      </div>
      <img
        class="home-gif"
        src="https://i.ibb.co/mCwfzXk/animation-640-kustg45t.gif"
        alt="Computer gif"
      />
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import NavDesktop from "./NavDesktop.vue";

export default defineComponent({
  name: "Home",
  components: {
    NavDesktop,
  },
});
</script>


<style lang="scss" scoped>
@import "../styles/variables";
.wrapper-nav {
  .nav-desktop {
    display: none;
  }
  .home-wrapper {
    display: flex;
    flex-direction: column;
    align-items: center;
    font-family: $font;
    background-color: $gray;
    .text-wrapper {
      text-align: right;
      width: 90%;
      .hello {
        font-size: 36px;
        color: $green;
        margin-top: 40px;
      }
      .iam {
        font-size: 48px;
        color: $pink;
        margin-top: 30px;
      }
      .profession {
        font-size: 18px;
        color: $pink;
        margin-top: 30px;
      }
      .icons-wrapper {
        display: flex;
        justify-content: space-evenly;
        margin-top: 40px;
        .icon {
          width: 50px;
        }
      }
    }
    .home-gif {
      width: 80%;
      margin-top: 10px;
      margin-bottom: 40px;
    }
  }
}

@media screen and (min-width: 1024px) {
  .wrapper-nav {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-evenly;
    background-color: $gray;
    height: 100vh;
    .nav-desktop {
      display: flex;
    }
    .home-wrapper {
      display: flex;
      flex-direction: row;
      justify-content: center;
      align-items: center;
      .text-wrapper {
        text-align: left;
        width: 40%;
        .hello {
          margin-top: 0px;
        }
        .icons-wrapper {
          display: flex;
          justify-content: flex-start;
          margin-top: 40px;
          .icon {
            width: 50px;
            margin-right: 40px;
            transition: all 300ms ease-in-out;
            &:hover {
              transform: scale(1.2);
            }
          }
        }
      }
      .home-gif {
        width: 40%;
      }
    }
  }
}
</style>