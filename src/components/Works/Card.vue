<template>
<div class="grid gap-4 grid-cols-1 md:grid-cols-3">
    <div v-for="work in works" :key='work.date' class="flex flex-warp">
        <div class="overflow-hidden rounded shadow-lg h-50 bg-gray-100 cursor-pointer" v-on:click="toggleModal(work)">
           <img class="object-contain" v-bind:src="require('@/assets/' + work.image.display)" v-on:mouseover="mouseover(work)" v-on:mouseleave="mouseleave(work)"/>
            <div class="p-4">
                <h3>{{work.title}}</h3>
                <p class="my-2 text-base mx-1">{{work.abstract}}</p>
                <p class="tag" v-for="category in work.categories"  :key="category.index">{{category}}</p> 
            </div>                 
        </div>
        <Modal v-if="showModal==work.title" v-bind:work="work" v-on:close="toggleModal(work)"></Modal>
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
        toggleModal(work){
            if(!this.showModal){
                this.showModal = work.title;
            } else {
                this.showModal =false;
            }
            
        },
        mouseover: function(work){
            if(work.image.hover){
                work.image.display= work.image.hover;
            }
        },
        mouseleave: function(work){
            if(work.image.leave){
                work.image.display= work.image.leave;
            }
        }
    }
}
</script>