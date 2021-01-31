<template>
  <div class="w-full text-left p-3 mt-5">
    <h1>Works</h1>
    <section class="my-4">
    <Card :works="works.contents"></Card>
    </section>
    
  </div>
</template>

<script>
import Card from "./Card.vue";
import axios from "axios";
export default {
  name: "work",
  data() {
    return {
      showModal: false,
      works: [],
    }
  },
  components: {
    Card,
  },
  async mounted() {
    // Worksを取得
    //秘密にする必要がないため公開してます。
    const response = await axios.get(
      "https://yukyu-myportfolio.microcms.io/api/v1/works",
      {
        headers: { "X-API-KEY": process.env.VUE_APP_X_API_KEY}
      }
    );
    this.works = response.data;
  }
};
</script>