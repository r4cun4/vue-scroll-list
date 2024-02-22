<script setup>
import ScrollList from '@/components/ScrollList.vue'
import Form from '@/components/Form.vue'
import { items } from '@/assets/data.json'

</script>

<template>
  <main class="flex flex-row items-center justify-center w-screen h-screen gap-20 bg-sky-900">
    <ScrollList :item="items" />
    <Form :item="items" />
  </main>
  
</template>
