<template>
  <section class="about-wrapper">
    <div class="first-block">
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
          first time I developed my first film roll. So in 2020 I moved out of
          my natal Tenerife to Barcelona. And in 2021, I focused my professional
          career on web development, a passion I always had.
        </p>
        <p class="article-text">
          Trained at Skylab Coders Academy (now ISDI Coders),
          <span class="decoration-text">world's best bootcamp</span> of 2021
          (according to SwitchUp), I keep learning about all the new
          technologies I find challenging.
        </p>
      </article>
      <article class="article-wrapper">
        <h2 class="article-title">Experience</h2>
        <p class="article-text">
          Due my past working as photographer, I love to pay special attention
          to details. I really love frontend because I think it has many things
          in common with composition in photography. I learned to be patient and
          wait for the perfect light and moment to shot a photo, so now I use
          these skills to understand and write my code.
        </p>
        <p class="article-text">
          My past as seller, allows me to empathize with every kind of person
          and to work in groups. I truly care about people and their problems.
        </p>
        <a
          class="decoration-text"
          href="https://pdfhost.io/v/y1WMEXd68_CV_Lola_Rufino_English"
          target="_blank"
          rel="noopener"
          >Download my CV</a
        >
      </article>
    </div>
    <div class="second-block">
      <article class="article-wrapper">
        <h2 class="article-title">Skills</h2>
        <p class="article-text">
          Normally, for frontend I like to use
          <span class="decoration-text">Typescript</span> and
          <span class="decoration-text">Javascript</span> for backend. I really
          like to alternate between the languages. For the frontend area I know
          how to work with HTML, CSS, SASS and BEM. I have developed with Vue
          using Vuex and React using Redux to apply
          <span class="decoration-text">Flux pattern</span>. For the backend
          area I know how to work with NodeJS, ExpressJS, MongoDB, Mongoose,
          PostMan, Passport, JWT, API Restful. I always test my code with unit
          test using Jest. Other technologies I like to use: Git, GitHub,
          SonarQube, EsLint, Trello, Slack, Excalidraw, Figma, Notion.
        </p>
      </article>
      <article class="article-wrapper">
        <img
          class="portrait"
          src="https://i.ibb.co/z7fc4vQ/004.jpg"
          alt="Illustration of a Lola's portrait"
        />
      </article>
    </div>
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
  .first-block {
    width: 85%;
    .article-wrapper {
      display: flex;
      flex-direction: column;
      margin-top: 20px;
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
    }
  }
  .second-block {
    width: 85%;
    .article-wrapper {
      display: flex;
      flex-direction: column;
      margin-top: 20px;
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
}
@media screen and (min-width: 860px) {
  .about-wrapper {
    padding-top: 40px;
    padding-bottom: 40px;
    .first-block {
      display: flex;
      flex-direction: row;
      justify-content: space-around;
      padding-top: 0;
      padding-bottom: 0;
      .article-wrapper {
        width: 40%;
        margin-top: 0;
      }
    }
    .second-block {
      display: flex;
      flex-direction: row;
      justify-content: space-around;
      align-items: center;
      .article-wrapper {
        width: 40%;
        margin-top: 0;
      }
    }
  }
}
</style>