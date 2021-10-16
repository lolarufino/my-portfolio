<template>
  <nav class="nav-wrapper">
    <div class="icon-text-wrapper">
      <a href="#home">
        <img
          class="icon"
          src="https://i.ibb.co/8NpCjyC/housecolored.png"
          alt="Home icon"
        />
        <p class="text">Home</p></a
      >
    </div>
    <div class="icon-text-wrapper">
      <a href="#about">
        <img
          class="icon"
          src="https://i.ibb.co/wBxMbcb/womancolored.png"
          alt="About icon"
        />
        <p class="text">About</p></a
      >
    </div>
    <div class="icon-text-wrapper">
      <a href="#projects">
        <img
          class="icon"
          src="https://i.ibb.co/bvq5ySC/codingcolored.png"
          alt="Projects icon"
        />
        <p class="text">Projects</p></a
      >
    </div>
    <div class="icon-text-wrapper">
      <a href="#contact">
        <img
          class="icon"
          src="https://i.ibb.co/5KMnN03/agendacolored.png"
          alt="Contact icon"
        />
        <p class="text">Contact</p></a
      >
    </div>
  </nav>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "NavDesktop",
});
</script>

<style lang="scss" scoped>
@import "../styles/variables";
.nav-wrapper {
  padding-top: 60px;
  background-color: $gray;
  display: flex;
  font-family: $font;
  .icon-text-wrapper {
    width: 90px;
    a {
      display: flex;
      flex-direction: column;
      align-items: center;
      .icon {
        width: 40px;
        transition: all 400ms ease-in-out;
        &:hover {
          transform: translateY(-20px);
        }
        &:hover ~ .text {
          visibility: visible;
          animation: text 0.5s ease-in-out;
        }
      }
      .text {
        visibility: hidden;
        color: $green;
      }
    }
  }
}
@keyframes text {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
</style>