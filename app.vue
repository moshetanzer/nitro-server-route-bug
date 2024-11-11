<script setup lang="ts">
const {data: broken} = await useFetch('/api/broken/testtoken', {
  method: 'GET',
  server: false
})
const {data: working} = await useFetch('/api/working/testtoken', {
  method: 'GET',
  server: false
})
</script>
<template>
  <div>
    <div>broken - {{ broken }}</div>
    <div>working - {{ working }}</div>
  </div>
</template>
