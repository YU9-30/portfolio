<template>
<div class="w-full text-left p-3 mt-5">
  <h1 class="font-bold text-3xl">Works</h1>
  <section>
      <Card :works="works"></Card>
  </section>
  
</div>
</template>

<script>
import Card from './Card.vue'
export default {
  name: "work",
  components: {
   Card,
  },
    data() {
        return {
            works : [
            {
                title: 'Bumeshi!!',
                data: '2020/1/22',
                abstract: "『ネガティブなレビューがない飲食店レビューサイト』を目標に開発中",
                Links: [
                  {
                    url: 'https://github.com/YU9-30/bumeshi_web',
                    display_name: 'Github',
                  },
                  {
                    url: 'https://bumeshi-eat.herokuapp.com/',
                    display_name: 'Bumeshi!!'
                  }
                ],
            },
          
        ]
        }
    }
  
};
</script>