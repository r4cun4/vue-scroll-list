<script setup>
import ItemList from './ItemList.vue';

import { ref, watchEffect } from 'vue'

const props = defineProps({
    item: Object,
    input: Number,
    visibleItems: Number,
})

const scrollContainer = ref(null)
let accumulatedScrollTop = 0;
let card = 150

let totalHeight = card * props.visibleItems

const scrollTo = () => {
    if(scrollContainer.value){

        if(props.input === 1 ) {
            card = 0
        } else {
            card = 150
        }
        accumulatedScrollTop = card * (props.input -1)
        scrollContainer.value.scrollTo({
            top: accumulatedScrollTop,
            behavior: 'smooth'
        })
    }
}

watchEffect(() => {
    if (props.input !== 0 && props.input !== null) {
        scrollTo();
    }
});

</script>
<template>
    <div 
        ref="scrollContainer"
        class="scroll-container flex flex-col items-center overflow-hidden overflow-y-auto gap-4 bg-sky-950 w-96 shadow-md rounded p-1"
        :style="{ 'height': totalHeight + 'px' }">
        <ItemList v-for="item in props.item" :key="item.id" 
            :item="item"
        />
    </div>
</template>
