<template>
  <footer class="footer-wrapper">
    <div class="contact-wrapper">
      <div class="info-wrapper">
        <div class="title-wrapper">
          <h2 class="title">Let's connect!</h2>
        </div>
        <div class="email-wrapper">
          <p class="email-text">E-mail:</p>
          <div class="email-container">
            <span class="email">lola.ruf.ar@gmail.com</span>
          </div>
        </div>
        <p class="social-text">Social media accounts:</p>
        <div class="socialnetwork-wrapper">
          <div class="social-wrapper">
            <a href="https://www.linkedin.com/in/lola-rufino/" target="_blank"
              ><img
                class="social-icon"
                src="https://i.ibb.co/L0GzvnK/linkedin-2-green.png"
                alt="Linkedin icon"
            /></a>
          </div>
          <div class="social-wrapper">
            <a href="https://github.com/lolarufino" target="_blank"
              ><img
                class="social-icon"
                src="https://i.ibb.co/PQnQkh6/github-1-green.png"
                alt="Github icon"
            /></a>
          </div>
          <div class="social-wrapper">
            <a href="https://twitter.com/lolarufino" target="_blank"
              ><img
                class="social-icon"
                src="https://i.ibb.co/Bz7gbM3/gorjegreen.png"
                alt="Twitter icon"
            /></a>
          </div>
        </div>
      </div>
      <img
        class="footer-gif"
        src="https://i.ibb.co/9wvK33X/animation-640-kucts3zv.gif"
        alt="Gif of a personal computer"
      />
    </div>
    <span class="copyright-text">&copy; Lola Rufino 2021</span>
  </footer>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "Contact",
});
</script>


<style lang="scss">
@import "../styles/variables";
@import "../styles/extends";
.footer-wrapper {
  @extend %flex-column-center;
  justify-content: center;
  background-color: $bgpinkcontact;
  font-family: $font;
  .contact-wrapper {
    @extend %flex-column-center;
    .info-wrapper {
      width: 85%;
      @extend %flex-column-center;
      margin-top: 35px;
      .title-wrapper {
        @extend %titles-wrapper;
        .title {
          @extend %title;
          letter-spacing: 2px;
        }
      }
      .email-wrapper {
        display: flex;
        font-size: 14px;
        width: 80%;
        align-items: center;
        margin: 12px;
        .email-text {
          margin-right: 4px;
        }
        .email-container {
          background-color: $gray;
          padding: 3%;
          border-radius: 20px 0 20px 0;
          .email {
            color: $green;
          }
        }
      }
      .social-text {
        font-size: 14px;
        margin: 10px;
      }
      .socialnetwork-wrapper {
        width: 85%;
        display: flex;
        justify-content: space-evenly;
        display: flex;
        margin: 12px;
        .social-wrapper {
          @extend %icon-wrapper;
          .social-icon {
            @extend %icon;
          }
        }
      }
    }
    .footer-gif {
      width: 85%;
      margin: 12px;
    }
  }
  .copyright-text {
    margin: 12px;
    color: $gray;
    font-size: 14px;
    margin-bottom: 25px;
  }
}
@media screen and (min-width: 480px) {
  .footer-wrapper {
    .contact-wrapper {
      display: flex;
      flex-direction: row;
      justify-content: space-evenly;
      .info-wrapper {
        width: 40%;
        display: flex;
        align-items: flex-start;
        .email-wrapper {
          display: flex;
          flex-direction: column;
          align-items: flex-start;
          .email-container {
            margin-top: 15px;
            &:hover {
              transform: scale(1.2);
            }
          }
        }
        .socialnetwork-wrapper {
          display: flex;
          justify-content: flex-start;
          .social-wrapper {
            margin-right: 18px;
            &:hover {
              transform: scale(1.2);
            }
          }
        }
      }
      .footer-gif {
        width: 40%;
      }
    }
  }
}
</style>