<template>
  <div class="main-wrapper">
    <nav>
      <a href="#home">Home</a>
      <a href="#about">About</a>
      <a href="#projects">Projects</a>
      <a href="#contact">Contact</a>
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
      <a href="#about">
        <img
          class="arrow-wrapper"
          src="https://i.ibb.co/ftVfkXK/ahead-only.png"
          alt=""
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
html {
  scroll-behavior: smooth;
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
  .arrow-wrapper {
    display: none;
  }
}
@media screen and (min-width: 480px) {
  .main-wrapper {
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
}
</style>
