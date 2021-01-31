<template>
<div class="grid gap-4 grid-cols-1 md:grid-cols-3">
    <div v-for="work in works" :key='work.createdAt' class="flex flex-warp">
        <div class="overflow-hidden rounded shadow-lg h-50 bg-gray-100 cursor-pointer" v-on:click="toggleModal(work.id)">
           <img class="object-contain" v-bind:src="require('@/assets/' + work.images.default)"/>
            <div class="p-4">
                <h3>{{work.title}}</h3>
                <p class="my-2 text-base mx-1">{{work.abstract}}</p>
                <p class="tag" v-for="category in work.categories"  :key="category.index">{{category.name}}</p> 
            </div>                 
        </div>
        <Modal v-if="showModal==work.id" v-bind:work="work" v-on:close="toggleModal(work.id)"></Modal>
    </div>
</div>

</template>

<script>
import Modal from "./Modal.vue";

export default {
    props: ['works'],
    name: "Works",
    components: {
        Modal,
        
    },
    data() {
        return {
            showModal: false,
        }
    },

    methods: {
        toggleModal(id){
            if(!this.showModal){
                this.showModal = id;
            } else {
                this.showModal =false;
            }
            
        },
        
    }
}
</script>