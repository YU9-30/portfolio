<template>
<div class="w-full text-left p-3 mt-5">
  <h1 class="font-bold text-3xl text-normal-color">Works</h1>
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
                date: '2020/1/22',
                abstract: "『ネガティブなレビューがない飲食店レビューサイト』を目標に開発中です。",
                Links: [
                  {
                    url: 'https://github.com/YU9-30/bumeshi_web',
                    display_name: 'Github',
                  },
                  {
                    url: 'https://bumeshi-eat.herokuapp.com/',
                    display_name: 'Bumeshi!!'
                  },
                  {
                    url: 'https://zenn.dev/yu_9/articles/yu9-bumeshi-2021',
                    display_name: 'Zennの記事'
                  }
                ],
            },
            {
                title: 'BECCHU',
                date: '2020/1/22',
                abstract: "『クリエイターさんのデザイン守りつつ、オンリーワンを作る』を目標に開発しました。",
                Links: [
                  {
                    url: 'https://github.com/YU9-30/bumeshi_web',
                    display_name: 'Github',
                  },
                  {
                    url: 'http://becchu.yu-9.work/',
                    display_name: 'BECCHU'
                  },
                  {
                    url: 'https://zenn.dev/yu_9/articles/yu9-becchu-2021',
                    display_name: 'Zennの記事'
                  }
                ],
            },
          
        ]
        }
    }
  
};
</script>