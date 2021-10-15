<template>
  <div class="projects-wrapper">
    <SingleProject
      stack="#Vue #Vuex #Typescript #SASS #MongoDB #Express #Passport #Vercel #Notion"
      description="Website where you can, given a filter, check in wich film photography lab you can develop your film."
      deploylink="https://revela-and-go.vercel.app/"
      githublink="https://github.com/lolarufino/revela-and-go"
      title="Revela & Go"
      src="https://i.ibb.co/RSv84Cg/mockup-revela-and-gosamll.png"
    />
    <SingleProject
      stack="#Vue #Vuex #Typescript #SASS #Vercel #Eslint #SonarQube #Github"
      description="Simple To Do List where you can add new tasks, delete tasks, update tasks, complete tasks and filter by state."
      deploylink="https://todolist-vue-lolarufino.vercel.app/"
      githublink="https://github.com/lolarufino/todolist-vue"
      title="To Do List Vue"
      src="https://i.ibb.co/Bq1Nk4M/pf-s73-eve-set-14-mockupsmall.png"
    />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import SingleProject from "../components/SingleProject.vue";

export default defineComponent({
  name: "Projects",
  components: {
    SingleProject,
  },
});
</script>


<style lang="scss">
@import "../styles/variables";
.projects-wrapper {
  background-color: $gray;
  padding-top: 40px;
  padding-bottom: 40px;
  display: flex;
  flex-direction: column;
  align-items: center;
}
@media screen and (min-width: 860px) {
  .projects-wrapper {
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
  }
}
</style>