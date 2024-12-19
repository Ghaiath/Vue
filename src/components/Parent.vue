<template>
  <h2>This is the Parent</h2>
  <button @click="toggleChild">Toggle Child</button>
  <Child v-if="showChild" />
</template>

<script setup>
import { onBeforeMount, onBeforeUpdate, 
  onMounted, onUpdated, ref } from 'vue';

import Child from './Child.vue';

const showChild = ref(true)

const toggleChild = () => {
  showChild.value = !showChild.value
}

console.log("Parent Created");

onBeforeMount(() => {
  console.log("Parent onBeforeMount");
})

onMounted(() => {
  console.log("Parent onMounted");
})

onBeforeUpdate(() => {
  console.log("Parent onBeforeUpdate");
})

onUpdated(() => {
  console.log("Parent onUpdated");
})

</script>