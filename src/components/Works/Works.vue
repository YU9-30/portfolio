<template>
  <div class="w-full text-left p-3 mt-5">
    <h1>Works</h1>
    <h2 class="pl-2 mt-7">アプリケーション</h2>
    <section class="mb-4">
      <Card :works="apps"></Card>
    </section>
    <h2 class="pl-2 mt-10">制作物</h2>
      <Card :works="creations"></Card>
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
      apps: [
        {
          title: "クリエイターサポートツール",
          date: "2019/01/22",
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
              url: "https://github.com/YU9-30/suzuri_support_tool",
              display_name: "ソースコード(Github)",
            },
          ],
        },
        {
          title: "BECCHU",
          date: "2020/11/1",
          abstract: "デザインと色を選ぶことでTシャツなどを作成できるWEBアプリケーション",
          image: {
            display: "work/becchu.jpg",
            leave: "work/becchu.jpg",
            hover: "work/becchu.gif",
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
              url: "https://github.com/YU9-30/semiorder_suzuri",
              display_name: "ソースコード(Github)",
            },
          ],
        },
        {
          title: "Bumeshi!!",
          date: "2021/01/10",
          image: {
            display: "work/bumeshi.jpg",
            leave: "work/bumeshi.jpg",
            hover: "work/bumeshi.gif",
          },
          abstract: "美味しい飲食店を共有するWEBアプリケーション",
          categories: [
            "Ruby",
            "Ruby on Rails",
            "WEBアプリケーション",
            "ぐるなび API",
            "モバイルアプリケーション"
          ],
          links: [
            {
              url: "https://bumeshi-eat.herokuapp.com/",
              display_name: "Bumeshi!!(起動に時間がかかります)",
            },
            {
              url: "https://zenn.dev/yu_9/articles/yu9-bumeshi-2021",
              display_name: "詳細(Zenn)",
            },
            {
              url: "https://github.com/YU9-30/bumeshi_web",
              display_name: "ソースコード(Github)",
            },
            {
              url: "https://note.com/yukyu/m/m5b87dbecdee1",
              display_name: "Flutter版Bumeshi!! 開発日記(note)",
            },
          ],
        },
      ],
      creations: [
        {
          title: "3Dモデル",
          date: "2021/1/10",
          image: {
            display: "work/avater.jpg",
            leave: "work/avater.jpg",
            hover: "work/avater-posed.png",
          },
          abstract: "humanoid型のフルスクラッチ3Dモデル",
          categories: [
            "Blender",
            "モデリング",
            "VR",
          ],
          links: [
            {
              url: "https://www.fanbox.cc/@yu-9/posts/1817823",
              display_name: "詳細(Pixiv Fanbox)",
            },
          ],
        },
        {
          title: "FORGER",
          date: "2021/1/10",
          image: {
            display: "work/forger-box.jpg",
            leave: "work/forger-box.jpg",
            hover: "work/forger-unbox.jpg",
          },
          abstract: "3Dプリンターで作成したボールペン",
          categories: [
            "3Dプリンター",
            "Fusion360",
            "文具",
          ],
          links: [
            {
              url: "https://note.com/yukyu/n/n90b7e7aa3d89",
              display_name: "開発日記(note)",
            },
          ],
        },
        {
          title: "yu9logos",
          date: "2019/01/26",
          image: {
            display: "work/yu9logos-example.jpg",
            leave: "work/yu9logos-example.jpg",
            hover: "work/yu9logos.jpg",
          },
          abstract: "ロゴを作成時にうまれた文字をフォント化したもの",
          categories: ["Affinity Designer", "デザイン", "フォント"],
          links: [
            {
              url: "https://uq-konpeki-dou.booth.pm/items/2321072",
              display_name: "ダウンロード先(Booth)",
            },
            {
              url: "https://www.fanbox.cc/@yu-9/tags/yu9logos%E3%81%AE%E9%80%B2%E6%8D%97%E5%A0%B1%E5%91%8A",
              display_name: "フォント作成進捗報告(Pixiv Fanbox)",
            },
          ],
        },
        {
          title: "服装予報",
          date: "2019/03/24",
          abstract: "気温から適した服装を教えてくれる装置",
          image: {
            display: "work/fukusouyohou.jpg",
            leave: "work/fukusouyohou.jpg",
            hover: "work/fukusouyohou.gif",
          },
          categories: ["M5Stack", "電子工作"],
          links: [
            {
              url: "https://www.shumi-tech.online/entry/2019/03/24/%E6%9C%80%E9%AB%98%E6%B0%97%E6%B8%A9%E3%81%8B%E3%82%89%E9%81%A9%E5%88%87%E3%81%AA%E6%9C%8D%E8%A3%85%E3%82%92%E6%95%99%E3%81%88%E3%81%A6%E3%81%8F%E3%82%8C%E3%82%8B%E8%A3%85%E7%BD%AE%E3%82%92%E4%BD%9C",
              display_name: "投稿記事(趣味TECHオンライン)",
            },
          ],
        },
        
      ],
    };
  },
};
</script>