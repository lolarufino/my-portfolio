<template>
  <section class="project-wrapper">
    <p class="stack">{{ stack }}</p>
    <p class="description">{{ description }}</p>
    <div class="links-wrapper">
      <a :href="deploylink" target="_blank"
        ><img
          class="deploylink"
          src="https://i.ibb.co/4dWQCqj/enlacegreen.png"
          alt="Link icon"
        />Deploy</a
      >
      <a :href="githublink" target="_blank"
        ><img
          class="githublink"
          src="https://i.ibb.co/g79GY6c/github-1-green.png"
          alt="Github logo"
        />
        Github</a
      >
    </div>
    <h3 class="title">{{ title }}</h3>
    <img class="preview" :src="src" />
  </section>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "SingleProject",
  props: ["stack", "description", "deploylink", "githublink", "title", "src"],
});
</script>

<style lang="scss" scoped>
@import "../styles/variables";
a {
  width: 60px;
  margin-right: 10px;
  margin-left: 10px;
}
.project-wrapper {
  display: flex;
  flex-direction: column;
  align-items: center;
  font-family: $font;
  width: 85%;
  margin-bottom: 40px;
  .stack {
    color: $green;
    text-shadow: 1px 1px 0 $bgpinkabout;
    margin-bottom: 10px;
  }
  .description {
    color: $bgpinkabout;
    margin-bottom: 25px;
  }
  .links-wrapper {
    display: flex;
    justify-content: center;
    align-items: center;
    .deploylink {
      width: 50px;
      box-shadow: 1px 1px 4px $bgpinkabout;
      border-radius: 0 10px 0 10px;
    }
    .githublink {
      width: 50px;
      box-shadow: 1px 1px 4px $bgpinkabout;
      border-radius: 0 10px 0 10px;
    }
  }
  .title {
    color: $green;
    text-shadow: 1px 1px 0 $bgpinkabout;
    font-size: 36px;
    margin-bottom: 10px;
  }
  .preview {
    border-radius: 0 40px 0 40px;
    width: 100%;
    box-shadow: 2px 2px 0 $bgpinkabout;
  }
}
</style>
