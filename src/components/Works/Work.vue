<template>
  <div class="w-full text-left p-3 mt-5">
    <h1 class="font-bold text-3xl text-normal-color">Works</h1>
    <section>
      <Card :works="works"></Card>
    </section>
  </div>
</template>

<script>
import Card from "./Card.vue";
export default {
  name: "work",
  components: {
    Card,
  },
  data() {
    return {
      works: [
        {
          title: "クリエイターサポートツール",
          date: "2019/1/22",
          image: {
            display: "work/CST.jpg",
            leave: "work/CST.jpg",
            hover: "work/CST.gif",
          },
          abstract: "SUZURIのPR画像を生成できるWEBアプリケーション",
          categories: ["PHP", "WEBアプリケーション", "SUZURI API"],
          links: [
            {
              url: "https://creator-support-tool.yu-9.work/",
              display_name: "クリエイターサポートツール",
            },
            {
              url: "https://zenn.dev/yu_9/articles/5fa3a6c9332afd",
              display_name: "詳細(Zenn)",
            },
            {
              url: "https://github.com/YU9-30/bumeshi_web",
              display_name: "Github",
            },
          ],
        },
        {
          title: "BECCHU",
          date: "2020/11/1",
          abstract: "デザインと色を選ぶことでTシャツなどを作成できるWEBアプリケーション",
          image: {
            display: "icon.jpg",
            leave: "icon.jpg",
            hover: "work/CST.gif",
          },
          categories: ["PHP", "Laravel", "WEBアプリケーション", "SUZURI API"],
          links: [
            {
              url: "http://becchu.yu-9.work/",
              display_name: "BECCHU",
            },
            {
              url: "https://zenn.dev/yu_9/articles/yu9-becchu-2021",
              display_name: "詳細(Zenn)",
            },
            {
              url: "https://github.com/YU9-30/bumeshi_web",
              display_name: "Github",
            },
          ],
        },
        {
          title: "Bumeshi!!",
          date: "2021/1/10",
          image: {
            display: "work/CST.gif",
            leave: "icon.jpg",
            hover: "work/CST.gif",
          },
          abstract: "美味しい飲食店を共有するWEBアプリケーション",
          categories: [
            "Ruby",
            "Ruby on Rails",
            "WEBアプリケーション",
            "ぐるなび API",
          ],
          links: [
            {
              url: "https://bumeshi-eat.herokuapp.com/",
              display_name: "Bumeshi!!",
            },
            {
              url: "https://zenn.dev/yu_9/articles/yu9-bumeshi-2021",
              display_name: "詳細(Zenn)",
            },
            {
              url: "https://github.com/YU9-30/bumeshi_web",
              display_name: "Github",
            },
          ],
        },
      ],
    };
  },
};
</script>