<template>
  <div class="rounded-lg shadow-lg bg-gray-100 w-full flex flex-row flex-wrap p-3">
    <div class="md:w-1/3 w-full">
        <img class="object-cover w-full h-60 rounded-lg" src="@/assets/icon.jpg">
    </div>
    <div class="md:w-2/3 flex justify-center items-center w-full">
      <div class="text-center text-blue-900 font-semibold relative pt-3 mx-3 md:pt-0">
        <p class="text-3xl">{{ name }}</p>
        <div class="flex">
          <div class="flex-auto mt-1">
            <p class="text-base">生年月日：{{ birthday }}</p>
          </div>
        </div>
        <Links class="mt-5"></Links>
      </div>
      
    </div>
  </div>
</template>

<script>
import Links from './Link.vue'
export default {
  name: "ProfileCard",
  components: {
    Links
  },
  data() {
    return {
      name: "悠久",
      name_kana: "ゆうきゅう",
      birthday: "199X/9/30"
      
    };
  },
};
</script>