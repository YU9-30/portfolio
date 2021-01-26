<template>
  <div class="bg-white w-screen h-screen flex flex-row flex-wrap p-3">
    <div class="w-full m-2 md:mx-auto md:w-2/3">
      <Header></Header>
      <Works></Works>
      
    </div>
  </div>
</template>

<script>
import Header from './components/Header/ProfileCard.vue'
import Works from './components/Works/Works.vue'

export default {
  name: 'App',
  components: {
   Header,
   Works,
  }
}
</script>

<style>

</style>
