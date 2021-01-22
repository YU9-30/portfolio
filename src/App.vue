<template>
  <div class="w-screen h-screen bg-white flex flex-row flex-wrap p-3">
    <div class="w-full m-2 md:mx-auto md:w-2/3">
      <Header></Header>
      <Work></Work>
    </div>
  </div>
</template>

<script>
import Header from './components/Header/Card.vue'
import Work from './components/Works/Work.vue'

export default {
  name: 'App',
  components: {
   Header,
   Work,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
