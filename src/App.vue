<template>
  
  <div class="w-full h-full flex flex-row flex-wrap" > 
    <div class="overflow-hidden z-0 fixed" id="canvas"></div>
    <div class="w-full m-2 md:mx-auto md:w-2/3 z-10">
      <Header></Header>
      <Works></Works>
      <Skills></Skills>
      
    </div>
  </div>
</template>

<script>
import Header from './components/Header/ProfileCard.vue'
import Works from './components/Works/Works.vue'
import Skills from './components/Skills/Skills.vue'
import P5 from 'p5'

export default {
  name: 'App',
  components: {
   Header,
   Works,
   Skills,
  },
  created() {
    const sketch = s => {
        let w = window.innerWidth;
        let h = window.innerHeight;

        s.setup = () => {
            s.createCanvas(w, h);
        };

        s.draw = () => {
            s.background(33, 33, 33);
            s.ellipse(50, 50, 100, 100);

            
        };

        
    }

    new P5(sketch, 'canvas');
}
}
</script>

<style>

</style>
