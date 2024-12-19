<template>
  <h2>This is the Child</h2>
</template>

<script setup>
import { onBeforeMount, onBeforeUnmount, 
  onMounted, onUnmounted } from 'vue';

console.log("Child Created");

onBeforeMount(() => {
  console.log("Child onBeforeMount");
})

onMounted(() => {
  console.log("Child onMounted");
})

onBeforeUnmount(() => {
  console.log("Child onBeforeUnmount");
})

onUnmounted(() => {
  console.log("Child onUnmounted");
})

</script>