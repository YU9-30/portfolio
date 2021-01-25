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
                title: 'クリエイターサポートツール',
                md: 'bumeshi.md',
                date: '2019/1/22',
                abstract: "『PR画像をもっと気軽に作れるようにしたい』を目標に開発しました。",
                category: [
                  'PHP', 'WEBアプリケーション' 
                ],
                links: [
                  {
                    url: 'https://github.com/YU9-30/bumeshi_web',
                    display_name: 'Github',
                  },
                  {
                    url: 'https://creator-support-tool.yu-9.work/',
                    display_name: 'クリエイターサポートツール'
                  },
                  {
                    url: 'https://zenn.dev/yu_9/articles/5fa3a6c9332afd',
                    display_name: '詳細(Zenn)'
                  }
                ],
            },
            {
                title: 'BECCHU',
                md: 'bumeshi.md',
                date: '2020/11/1',
                abstract: "『クリエイターさんのデザイン守りつつ、オンリーワンを作る』を目標に開発しました。",
                category: [
                  'PHP', 'Laravel', 'WEBアプリケーション' 
                ],
                links: [
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
                    display_name: '詳細(Zenn)'
                  }
                ],
            },
            {
                title: 'Bumeshi!!',
                md: 'bumeshi.md',
                date: '2021/1/10',
                abstract: "『ネガティブなレビューがない飲食店レビューサイト』を目標に開発中です。",
                category: [
                  'Ruby', 'Ruby on Rails', 'WEBアプリケーション' 
                ],
                links: [
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
                    display_name: '詳細(Zenn)'
                  }
                ],
            },
            
          
        ]
        }
    }
  
};
</script>