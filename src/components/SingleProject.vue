<template>
  <section class="project-wrapper">
    <p class="stack">{{ stack }}</p>
    <p class="description">{{ description }}</p>
    <div class="links-wrapper">
      <a :href="deploylink" target="_blank" rel="noopener"
        ><img
          class="deploylink"
          src="https://i.ibb.co/4dWQCqj/enlacegreen.png"
          alt="Link icon"
        />Deploy</a
      >
      <a :href="githublink" target="_blank" rel="noopener"
        ><img
          class="githublink"
          src="https://i.ibb.co/g79GY6c/github-1-green.png"
          alt="Github logo"
        />
        Github</a
      >
    </div>
    <h3 class="title">{{ title }}</h3>
    <img class="preview" :src="src" alt="Preview of project" />
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
    text-shadow: 1px 1px 0 $pink;
    margin-bottom: 10px;
    order: 4;
  }
  .description {
    color: $pink;
    margin-bottom: 25px;
    order: 5;
  }
  .links-wrapper {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 20px;
    order: 3;
    .deploylink {
      width: 50px;
    }
    .githublink {
      width: 50px;
    }
  }
  .title {
    color: $green;
    text-shadow: 1px 1px 0 $pink;
    font-size: 36px;
    margin-bottom: 10px;
    order: 1;
  }
  .preview {
    border-radius: 0 40px 0 40px;
    width: 100%;
    box-shadow: 2px 2px 0 $pink;
    order: 2;
  }
}
@media screen and (min-width: 860px) {
  .project-wrapper {
    margin-top: 30px;
    width: 35%;
    .stack {
      order: 2;
    }
    .description {
      order: 3;
    }
    .links-wrapper {
      margin-top: 0;
      order: 4;
      .deploylink {
        transition: all 300ms ease-in-out;
        &:hover {
          transform: scale(1.2);
        }
      }
      .githublink {
        transition: all 300ms ease-in-out;
        &:hover {
          transform: scale(1.2);
        }
      }
    }
    .title {
      order: 1;
    }
    .preview {
      order: 5;
    }
  }
}
</style>
