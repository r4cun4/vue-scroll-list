<script setup>

const props = defineProps({
    item: Object
})

</script>
<template>
    <article class="w-38 bg-pink-500 p-4 rounded">
        <img :src="item.avatar" alt="avatar image">
        <div>
            <h3 class="text-white text-center">{{ item.name }}</h3>
            <p class="text-white text-center">{{ item.rol }}</p>
        </div>
    </article>
</template>
