<template>
<div class="w-screen h-screen bg-white flex flex-row flex-wrap p-3">
  <div class="mx-auto w-2/3">
  <div class="rounded-lg shadow-lg bg-gray-100 w-full flex flex-row flex-wrap p-3">
    <div class="md:w-1/3 w-full">
        <img class="rounded-lg" src="@/assets/icon.jpg">
    </div>
    <div class="md:w-2/3 flex justify-center items-center w-full px-3 flex flex-row flex-wrap">
      <div class="w-full text-left text-blue-700 font-semibold relative pt-3 mx-3 md:pt-0">
        <div class="text-2xl text-blue-500 leading-tight">悠久</div>
      </div>
    </div>
  </div>
  </div>
</div>
</template>

<script>
export default {
  name: "header",
  data() {
    return {
      msg: "Welcome to Myportfolio",
    };
  },
};
</script>