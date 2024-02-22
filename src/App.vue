<script setup>
import ScrollList from '@/components/ScrollList.vue'
import Form from '@/components/Form.vue'
import { items } from '@/assets/data.json'
import { ref } from 'vue'

const inputValue = ref(null)

const handleFormSubmit = (input) => {

  inputValue.value = input

}

</script>

<template>
  <main class="flex flex-row items-center justify-center w-screen h-screen gap-20 bg-sky-900">
    <ScrollList :item="items" :input="inputValue" />
    <Form :item="items" @submit="handleFormSubmit" />
  </main>
  
</template>
