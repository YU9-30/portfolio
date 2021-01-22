<template>

    <div v-for="work in works" :key='work.data'>
        <div class="p-10 md:w-1/3 md:mb-0 mb-6 flex flex-col ">
        <div class="pattern-dots-md red">
            <div class="rounded bg-gray-800 p-4 transform translate-x-6 -translate-y-6">
                <div class="w-10 h-10 inline-flex items-center justify-center rounded-full bg-green-100 text-green-500 mb-5 flex-shrink-0 p-2">
                    <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 21a4 4 0 01-4-4V5a2 2 0 012-2h4a2 2 0 012 2v12a4 4 0 01-4 4zm0 0h12a2 2 0 002-2v-4a2 2 0 00-2-2h-2.343M11 7.343l1.657-1.657a2 2 0 012.828 0l2.829 2.829a2 2 0 010 2.828l-8.486 8.485M7 17h.01"></path></svg>                </div>
                <div class="flex-grow ">
                    <h2 class=" text-xl title-font font-medium mb-3">Webdesign</h2>
                    <p class="leading-relaxed text-sm text-justify">Donner du goût 😍 de la couleur aux applications, je le fais afin de rendre vos sites attrayants 🎨. Avant de devenir webdesigner, depuis tout petit j'étais déjà familier à la couleur et du dessin.</p>
                </div>
            </div>
        </div>
        </div>
    <button class="bg-pink-500 text-white active:bg-pink-600 font-bold uppercase text-sm px-6 py-3 rounded shadow hover:shadow-lg outline-none focus:outline-none mr-1 mb-1" type="button" style="transition: all .15s ease" v-on:click="toggleModal()">
      {{ work.title }}
    </button>
    <div v-if="showModal" class="overflow-x-hidden overflow-y-auto fixed inset-0 z-50 outline-none focus:outline-none justify-center items-center flex">
      <div class="relative w-auto my-6 mx-auto max-w-3xl">
        <!--content-->
        <div class="border-0 rounded-lg shadow-lg relative flex flex-col w-full bg-white outline-none focus:outline-none">
          <!--header-->
          <div class="flex items-start justify-between p-5 border-b border-solid border-gray-300 rounded-t">
            <h3 class="text-3xl font-semibold">
              {{ work.title }}
            </h3>
            <button class="h-8 w-8 text-red-500 bg-transparent border border-solid border-red-500 hover:bg-red-500 hover:text-white active:bg-red-600 font-bold text-sm p-1 rounded outline-none focus:outline-none" type="button" style="transition: all .15s ease" v-on:click="toggleModal()">
              ×
            </button>
          </div>
          <!--body-->
          <div class="relative p-6 flex-auto">
            <p class="my-4 text-gray-600 text-lg leading-relaxed">
              {{work.abstract}}
            </p>
          </div>
          <!--footer-->
          <div class="flex items-center justify-end p-6 border-t border-solid border-gray-300 rounded-b">
           
          </div>
        </div>
      </div>
    </div>
    <div v-if="showModal" class="opacity-25 fixed inset-0 z-40 bg-black"></div>
  </div>
</template>

<script>
export default {
    props: ['works'],
    name: "regular-modal",
    data() {
        return {
            showModal: false
        }
    },
    methods: {
        toggleModal: function(){
            this.showModal = !this.showModal;
        }
    }
}
</script>