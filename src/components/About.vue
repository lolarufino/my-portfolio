<template>
  <section class="about-wrapper">
    <article class="article-wrapper">
      <h2 class="article-title">Who am I?</h2>
      <p class="article-text">
        I went from <span class="decoration-text">photographer</span> to
        <span class="decoration-text">web developer</span>, deciding to change
        camera's "click" for the mouse's one.
      </p>
      <p class="article-text">
        The first time I wrote my first
        <span class="decoration-text">console.log()</span> I felt the same
        <span class="decoration-text">butterflies in my belly</span> than the
        first time I developed my first film roll. So in 2020 I moved out of my
        natal Tenerife to Barcelona. And in 2021, I focused my professional
        career on web development, a passion I always had.
      </p>
      <p class="article-text">
        Trained at Skylab Coders Academy (now ISDI Coders),
        <span class="decoration-text">world's best bootcamp</span> of 2021
        (according to SwitchUp), I keep learning about all the new technologies
        I find challenging.
      </p>
      <p class="article-text">
        My favourites <span class="decoration-text">technologies</span> are
        HTML5, CSS3, SASS, JavaScript (ES6), React (with Hooks), Redux, Vue and
        Vuex. I also love to use Figma and Notion for personal projects.
      </p>
    </article>
    <article class="article-wrapper">
      <img
        class="portrait"
        src="https://i.ibb.co/z7fc4vQ/004.jpg"
        alt="Illustration of a Lola's portrait"
      />
    </article>
  </section>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "About",
});
</script>


<style lang="scss" scoped>
@import "../styles/variables";
@import "../styles/extends";
.about-wrapper {
  background-color: $pink;
  font-family: $font;
  color: $gray;
  padding-top: 60px;
  padding-bottom: 60px;
  @extend %flex-column-center;
  .article-wrapper {
    display: flex;
    flex-direction: column;
    margin: 40px;
    .article-title {
      @extend %titles-wrapper;
      @extend %title;
      margin: 0;
      margin-bottom: 20px;
      align-self: flex-end;
    }
    .article-text {
      margin-bottom: 10px;
    }
    .decoration-text {
      color: $gray;
      text-shadow: 3px 3px 2px $green;
      text-decoration: none;
      font-weight: 900;
      transition: all 300ms ease-in-out;
      &:hover {
        text-shadow: 0px 0px 0px;
      }
    }
    .portrait {
      width: 90%;
      align-self: center;
    }
  }
}
@media screen and (min-width: 860px) {
  .about-wrapper {
    padding-top: 40px;
    padding-bottom: 40px;
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    .article-wrapper {
      width: 40%;
      margin-top: 0;
    }

    .article-wrapper {
      width: 40%;
      margin-top: 0;
    }
  }
}
</style>