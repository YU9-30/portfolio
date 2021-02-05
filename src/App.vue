<template>
  <div class="w-full h-screen flex flex-row flex-wrap">
    <div class="h-screen z-0 fixed" id="canvas"></div>
    <div class="w-full m-2 md:mx-auto md:w-2/3 z-10">
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
import P5 from "p5";

export default {
  name: "App",
  components: {
    Header,
    Works,
    Skills,
  },
 created() {
    const sketch = (s) => {
      let w = window.innerWidth;
      let h = window.innerHeight;

      s.setup = () => {
        s.createCanvas(w, h);
      };

      s.draw = () => {
        s.background(255);
        s.rectcross(w-w/6,200+(5*s.sin(s.frameCount/50)),2,100,100);
        
        s.rectcross(w-w/5.75,320+(5*s.sin(s.frameCount/50)),2,30,30);
        s.rectcross(w-w/8,350+(5*s.sin(s.frameCount/50)),2,40,40);
        s.rectcross(w/8,500+(5*s.sin(s.frameCount/50)),2,100,100);
        s.rectdots(w/8-100,500,3,15,5);
        s.rectcross(w/8-50,450+(5*s.sin(s.frameCount/50)),2,50,50);
        s.rectdots(w-100,h-300,3,10, 30);
        s.rectdots(60,350,3,15,3);
        s.rectdots(53,390,3,5,2);
        
        s.rectdots(w-w/3,0,3,4*s.sin((s.frameCount/360)+ 180 +s.cos(s.frameCount/50)*(2*(s.cos(s.frameCount/500))))+40,3);
      };
      s.rectcross = (x,y,size,w,h) =>{
        s.push()
        s.strokeWeight(1);
        s.stroke('#60A5FA');
        
        s.beginShape();
        s.line(x,y,x+w,y);
        s.line(x,y,x+w,y+h);
        s.line(x,y,x,y+h);
        s.line(x,y+h,x+w,y);
        s.line(x+w,y+h,x+w,y);
        s.line(x+w,y+h,x,y+h);
        s.noStroke();
        s.cross(x,y,size);
        s.cross(x+w,y,size);
        s.cross(x+w,y+h,size);
        s.cross(x,y+h,size);
        
        
        s.endShape();
        s.pop();
      };
      s.cross = (x,y,size) => {
       
        s.rectMode(s.CENTER);
        s.noStroke();
        s.fill('#2563EB');
        
        s.rect(x,y,1*size, 5*size);
        s.rect(x,y,5*size, 1*size);
      };
      s.rectdots = (x,y,size,w,h) => {
        s.push()
        s.rectMode(s.CORNER);
        s.noStroke();
        s.fill('#2563EB');
         s.beginShape();
         
        for(let i=0; i<w; i++){
          for(let j=0; j<h; j++){
            s.rect(x+(10*i),y+(10*j),size, size);
          }  
        }
         s.endShape();
        s.pop();
      };
    };
    new P5(sketch, "canvas");
  },
};
</script>

<style>
</style>
