<script setup>
import { ref, onBeforeMount } from 'vue';
const apiResponse = ref(null)

onBeforeMount(() => {
  fetch('https://jsonplaceholder.typicode.com/todos/1')
    .then(response => response.json())
    .then(json => {
      apiResponse.value = json
    })
})

</script>

<template>
  <p>{{ apiResponse }}</p>
</template>

<style scoped></style>
