<template>
  <div>
    <nav>
      <a href="#home">Home</a>
      <a href="#about">About</a>
      <a href="#projects">Projects</a>
      <a href="#contact">Contact</a>
    </nav>
    <Home id="home" />
    <About id="about" />
    <Projects id="projects" />
    <Contact id="contact" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import Home from "../src/components/Home.vue";
import About from "../src/components/About.vue";
import Projects from "../src/components/Projects.vue";
import Contact from "../src/components/Contact.vue";

export default defineComponent({
  components: {
    Home,
    About,
    Projects,
    Contact,
  },
});
</script>


<style lang="scss">
</style>
