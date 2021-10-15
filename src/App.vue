<template>
  <div class="main-wrapper">
    <NavDesktop class="nav-desktop" id="nav" />
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
      <a href="#nav">
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
import NavDesktop from "../src/components/NavDesktop.vue";

export default defineComponent({
  name: "App",
  components: {
    NavDesktop,
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
a {
  color: $gray;
}
.main-wrapper {
  overflow-x: hidden;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  height: 100vh;
  .nav-desktop {
    display: none;
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
    .nav-desktop {
      display: block;
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
}
</style>
