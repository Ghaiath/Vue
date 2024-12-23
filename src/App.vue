<template>
  <button @click="increament">Clicked {{ count }} times</button>
  <h1 @mouseover="increament">Hoverd {{ count }} times</h1>
</template>

<script setup>
import useCounter from './useCounter'

const { count, increament } = useCounter();

</script>
