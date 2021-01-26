<template>
    
        <div class="overflow-x-hidden overflow-y-auto text-blue-700 fixed inset-0 z-40 outline-none focus:outline-none justify-center items-center flex">
            <div class="relative w-auto my-6  max-w-3xl mx-1 md:mx-0">
                <!--content-->
                <div class=" h-screen-80 border-0  rounded-lg shadow-lg relative flex flex-col w-full bg-white outline-none focus:outline-none">
                    <!--header-->
                    <div class="flex h-20 items-start justify-between p-5 border-b border-solid border-gray-300 rounded-t">
                        <h3 class="text-3xl font-semibold">{{ work.title }}</h3>
                        <button class="h-8 w-8 overflow-hidden stroke-current text-red-500 bg-transparent border border-solid border-red-500 hover:border-gray-500 hover:text-gray-500 active:bg-red-600 font-bold text-sm rounded outline-none focus:outline-none" type="button" v-on:click="closeModal">
                            <svg class="stroke" width="100%" height="100%" viewBox="0 0 15 15" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" xml:space="preserve" xmlns:serif="http://www.serif.com/"><path d="M0,0l15,15"/><path d="M15,0l-15,15" /></svg>
                        </button>
                    </div>
                    <!--body-->
                    <div class="overflow-y-auto p-6">
                        <p class=" text-normal-color text-lg">
                        {{work.abstract}}
                        </p>
                        <img class="object-contain my-4" v-bind:src="require('@/assets/' + work.image.gif)"/>
                        <h3 class="font-bold text-normal-color">Link</h3>
                        <ul>
                            <li  v-for="link in work.links" :key='link.url' >
                                <a class="hover:text-blue-300" :href= link.url>
                                {{ link.display_name }}
                                </a>
                            </li>
                        </ul>
                        
                    </div>
                    <!--footer-->
                    <div class="p-6 h-20 border-gray-300 rounded-b">
                        <p class="tag" v-for="category in work.categories"  :key="category.index">{{category}}</p>                   
                    </div>
                </div>
            </div>
        </div>
    
        <div class="overflow-x-hidden overflow-y-auto pattern-dots-sm text-blue-700 fixed inset-0 outline-none focus:outline-none justify-left items-left ">
            <div class="opacity-25 fixed inset-0 bg-black"></div>
            <div class="opacity-60 text-9xl m-0 p-0 text-blue-700 z-1 font-black">
                <p>WORKS/</p>
                <p>{{work.title}}</p>
                
            </div>
        </div>
        
</template>

<script>

export default {
    props: ['work'],
    name: "work-modal",
    data() {
        return {
            showModal: false,

        }
    },
    methods: {
        closeModal:function(){
            this.$emit('close');
        }
    },
}
</script>