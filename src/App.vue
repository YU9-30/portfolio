<template>
  <div class="w-full flex flex-row flex-wrap bg-gray-50">
    
    <div class="w-full m-2 md:mx-auto md:w-2/3 z-10 ">
      <Header></Header>
      <Works></Works>
      <Skills></Skills>
    </div>
  </div>
</template>

<script>
import Header from "./components/Header/ProfileCard.vue";
import Works from "./components/Works/Works.vue";
import Skills from "./components/Skills/Skills.vue";

export default {
  name: "App",
  components: {
    Header,
    Works,
    Skills,
  },
 
};
</script>

<style>
</style>
