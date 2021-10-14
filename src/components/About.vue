<template>
  <section class="about-wrapper">
    <div class="first-block">
      <article class="article-wrapper">
        <h2 class="article-title">Who am I?</h2>
        <p class="article-text">
          I went from photographer to web developer, deciding to change camera's
          "click" for the mouse's one.
        </p>
        <p class="article-text">
          The first time I wrote my first console.log() I felt the same
          butterflies in my belly than the first time I developed my first film
          roll. So in 2020 I moved out of my natal Tenerife to Barcelona. And in
          2021, I focused my professional career on Web Development, a passion I
          always had.
        </p>
        <p class="article-text">
          Trained at Skylab Coders Academy (now ISDI Coders), world's best
          bootcamp of 2021 (according to SwitchUp), I keep learning about all
          the new technologies I find challenging.
        </p>
      </article>
      <article class="article-wrapper">
        <h2 class="article-title">Experience</h2>
        <p class="article-text">
          Due my past working as photographer, I love to pay special attention
          to details. I really love frontend because I think It has many things
          in common with composition in photography. I learned to be patient and
          wait for the perfect light and moment to shot a photo. I use these
          techniques now to understand and write my code. My past as seller,
          allows me to empathize with every kind of person and to work in
          groups. Now I can use all these skills for programming.
        </p>
        <span
          ><a
            class="cv"
            href="https://pdfhost.io/v/y1WMEXd68_CV_Lola_Rufino_English"
            target="_blank"
            >Download my CV</a
          ></span
        >
      </article>
    </div>
    <div class="second-block">
      <article class="article-wrapper">
        <h2 class="article-title">Skills</h2>
        <p class="article-text">
          Normally, for frontend I like to use Typescript and Javascript for
          backend. I really like to alternate between the languages. For the
          frontend area I know how to work with HTML, CSS, SASS and BEM. I have
          developed with Vue using Vuex and React using Redux to apply Flux
          pattern. For the backend area I know how to work with NodeJS,
          ExpressJS, MongoDB, Mongoose, PostMan, Passport, JWT, API Restful. I
          always test my code with unit test using Jest. Other technologies:
          Git, GitHub, SonarQube, EsLint, Trello, Slack, Excalidraw, Figma,
          Notion.
        </p>
        <img
          class="tea-gif"
          src="https://i.ibb.co/R0csQ9x/animation-640-kucsy693.gif"
          alt="Gif of a green tea"
        />
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

<style lang="scss">
@import "../styles/variables";
@import "../styles/extends";
.about-wrapper {
  background-color: $pink;
  font-family: $font;
  color: $gray;
  padding-top: 40px;
  padding-bottom: 40px;
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
      .cv {
        text-shadow: 3px 3px 2px $green;
        text-decoration: none;
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
      .tea-gif {
        display: none;
      }
      .portrait {
        width: 90%;
        align-self: center;
      }
    }
  }
}
</style>