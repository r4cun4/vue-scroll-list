<script setup>

const props = defineProps({
    item: Object
})

</script>
<template>
    <article class="grid grid-rows-3 grid-flow-col gap-4 bg-slate-100 p-3 rounded hover:bg-slate-200 w-60 h-36">
        <img 
            :src="item.avatar" 
            alt="avatar image"
            class="row-span-3  w-24 h-28"
        >
        <div class="row-span-2 col-span-2">
            <h3 class=" text-black text-center">{{ item.name }}</h3>
            <p class="text-black text-center">{{ item.rol }}</p>
            <p class="text-pink-500 font-bold text-center">#{{ item.id }}</p>
        </div>
    </article>
</template>
