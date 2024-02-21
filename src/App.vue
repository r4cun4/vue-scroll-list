<script setup>
import ScrollList from '@/components/ScrollList.vue'
import Form from '@/components/Form.vue'
import { items } from '@/assets/data.json'

</script>

<template>
  <main class="flex flex-row items-center justify-center bg-sky-950 w-screen h-screen gap-4">
    <ScrollList :item="items" />
    <Form :item="items" />
  </main>
  
</template>
