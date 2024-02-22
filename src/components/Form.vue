<script setup>

import { ref } from 'vue'

const props = defineProps({
    item: Object
})

const emit = defineEmits(['submit'])


const reset = () => {
    input.value = null
}

const submit = () => {
    emit('submit', input.value );
    reset()
};

const input = ref(null)

</script>
<template>
    <form @submit.prevent="submit" class="flex flex-col gap-2">
        <label for="" class="text-white">Add a number from 1 to 10</label>
        <input type="number" v-model="input">
        <button type="submit" class="bg-teal-500 rounded p-2 text-white font-bold hover:bg-teal-700">Submit</button>
    </form>
</template>
