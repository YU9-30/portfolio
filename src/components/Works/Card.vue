<template>
<div class="grid gap-4 grid-cols-1 md:grid-cols-3">
    <div v-for="work in works" :key='work.data' class="pt-3">
        <div class="rounded shadow-lg bg-gray-100 p-4 cursor-pointer" v-on:click="toggleModal()">
            <h2 class="text-xl title-font font-bold mb-3 text-normal-color">{{work.title}}</h2>
            <p class="text-gray-500"> {{work.title}}</p>                    
        </div>
     
        <div v-if="showModal" class="overflow-x-hidden overflow-y-auto pattern-dots-sm text-blue-700 fixed inset-0 z-50 outline-none focus:outline-none justify-left items-left ">
            
            <div class="overflow-x-hidden overflow-y-auto pattern-dots-sm text-blue-700 fixed inset-0 z-90 outline-none focus:outline-none justify-center items-center flex">
            <div v-if="showModal" class="relative w-auto my-6  max-w-3xl mx-1 md:mx-0">
                <!--content-->
                <div class="border-0 rounded-lg shadow-lg relative flex flex-col w-full bg-white outline-none focus:outline-none">
                <!--header-->
                
                <div class="flex items-start justify-between p-5 border-b border-solid border-gray-300 rounded-t">
                    <h3 class="text-3xl font-semibold">{{ work.title }}</h3>
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
        <h1 class="text-9xl m-0 p-0 font-black">WORKS</h1>
        </div>
    <div v-if="showModal" class="opacity-25 fixed inset-0 z-40 bg-black"></div>
  </div>
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