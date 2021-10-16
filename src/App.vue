<template>
  <div class="main-wrapper">
    <nav class="burger-menu">
      <div class="menu-toggle">
        <input class="checkbox" type="checkbox" />
        <span class="line"></span><span class="line"></span
        ><span class="line"></span>
        <div class="menu-list">
          <a class="list-text" href="#home"
            ><img
              class="icon"
              src="https://i.ibb.co/8NpCjyC/housecolored.png"
              alt="Home icon"
            />Home</a
          ><a class="list-text" href="#about"
            ><img
              class="icon"
              src="https://i.ibb.co/wBxMbcb/womancolored.png"
              alt="About icon"
            />About</a
          ><a class="list-text" href="#projects"
            ><img
              class="icon"
              src="https://i.ibb.co/bvq5ySC/codingcolored.png"
              alt="Projects icon"
            />Projects</a
          ><a class="list-text" href="#contact">
            <img
              class="icon"
              src="https://i.ibb.co/5KMnN03/agendacolored.png"
              alt="Contact icon"
            />Contact</a
          >
        </div>
      </div>
    </nav>
    <div id="home">
      <Home />
    </div>
    <div id="about">
      <About />
    </div>
    <div id="projects">
      <Projects />
    </div>
    <div id="contact">
      <Contact />
    </div>
    <div class="arrow-wrapper">
      <a href="#home">
        <img
          class="arrow-wrapper"
          src="https://i.ibb.co/ftVfkXK/ahead-only.png"
          alt="Arrow to navigate up in the page"
        />
      </a>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import Home from "../src/components/Home.vue";
import About from "../src/components/About.vue";
import Projects from "../src/components/Projects.vue";
import Contact from "../src/components/Contact.vue";

export default defineComponent({
  name: "App",
  components: {
    Home,
    About,
    Projects,
    Contact,
  },
  data() {
    return {};
  },
});
</script>


<style lang="scss">
@import "styles/variables";
* {
  margin: 0;
}
body {
  width: 100vw;
}
a {
  color: $gray;
}
.main-wrapper {
  overflow-x: hidden;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  height: 100vh;
  .burger-menu {
    font-family: $font;
    .menu-toggle {
      display: block;
      position: fixed;
      top: 30px;
      left: 30px;
      z-index: 1;
      background-color: $green;
      width: 50px;
      height: 50px;
      border-radius: 50%;
      .checkbox {
        display: block;
        width: 40px;
        height: 32px;
        position: absolute;
        top: 8px;
        left: 4px;
        cursor: pointer;
        opacity: 0;
        z-index: 2;
        &:checked ~ .line {
          opacity: 1;
          transform: rotate(45deg) translate(-2px, -1px);
          background: $green;
        }
        &:checked ~ .line:nth-last-child(3) {
          opacity: 0;
          transform: rotate(0deg) scale(0.2, 0.2);
        }
        &:checked ~ .line:nth-last-child(2) {
          transform: rotate(-45deg) translate(0, -1px);
        }
        &:checked ~ .menu-list {
          transform: none;
        }
      }
      .line {
        display: block;
        width: 33px;
        height: 4px;
        top: 14px;
        left: 8px;
        margin-bottom: 5px;
        position: relative;
        background: $gray;
        border-radius: 3px;
        z-index: 1;
        transform-origin: 4px 0px;
        transition: transform 0.5s cubic-bezier(0.77, 0.2, 0.05, 1),
          background 0.5s cubic-bezier(0.77, 0.2, 0.05, 1), opacity 0.55s ease;
        &:first-child {
          transform-origin: 0% 0%;
        }
        &:nth-last-child(2) {
          transform-origin: 0% 100%;
        }
      }
      .menu-list {
        border: 2px dotted $green;
        position: absolute;
        width: 50vw;
        height: 100vh;
        margin: -100px 0 0 -50px;
        padding: 50px;
        padding-top: 165px;
        background: $gray;
        transform-origin: 0% 0%;
        transform: translate(-100%, 0);
        transition: transform 0.5s cubic-bezier(0.77, 0.2, 0.05, 1);
        display: flex;
        flex-direction: column;
        align-items: flex-end;
        .list-text {
          font-size: 24px;
          text-decoration: none;
          color: $green;
          transition: color 0.3s ease;
          margin-top: 35px;
          .icon {
            width: 25px;
            margin-right: 10px;
          }
        }
      }
    }
  }
  .arrow-wrapper {
    display: none;
  }
}
@media screen and (min-width: 480px) {
  * {
    scroll-behavior: smooth;
  }
  .main-wrapper {
    .burger-menu {
      display: none;
    }
    .arrow-wrapper {
      display: block;
      position: fixed;
      bottom: 20px;
      right: 30px;
      z-index: 99;
      background-color: $gray;
      cursor: pointer;
      border-radius: 50%;
      width: 50px;
      height: 50px;
    }
  }
  ::-webkit-scrollbar {
    width: 13px;
    background-color: $gray;
  }
  ::-webkit-scrollbar-track {
    border: 1px solid $green;
    border-radius: 15px;
    background-color: $gray;
  }
  ::-webkit-scrollbar-thumb {
    background: $green;
    border-radius: 15px;
  }
}
</style>
