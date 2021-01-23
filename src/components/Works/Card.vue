<template>
<div class="grid gap-4 grid-cols-1 md:grid-cols-2">
    <div v-for="work in works" :key='work.date' class="pt-3">
        <div class="rounded shadow-lg bg-gray-100 p-4 cursor-pointer" v-on:click="toggleModal(work)">
            <h2 class="text-xl title-font font-bold mb-3 text-normal-color">{{work.title}}</h2>
            <p class="text-gray-500"> {{work.title}}</p>                    
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
            showModal: false
        }
    },
    methods: {
        toggleModal(work){
            if(!this.showModal){
                this.showModal = work.title;
            } else {
                this.showModal =false;
            }
            
        }
    }
}
</script>