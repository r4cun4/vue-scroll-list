<script setup>
import ItemList from './ItemList.vue';

import { ref } from 'vue'

const props = defineProps({
    item: Object,
    visibleItems: Number
})

</script>
<template>
    <div class="scroll-container flex flex-col items-center overflow-hidden overflow-y-auto gap-4 bg-sky-950 w-96 shadow-md rounded p-1">
        <ItemList v-for="item in props.item" :key="item.id" 
            :item="item"
        />
    </div>
</template>

<style>
.scroll-container {
    height: 47rem;
}

</style>