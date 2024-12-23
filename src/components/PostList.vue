<template>
  <div v-for="post in posts" :key="post.id">
    <h3>{{ post.id }}</h3>
    <h4>{{ post.title }}</h4>
    <h5>{{ post.body }}</h5>

    <h3></h3>
    <hr>
  </div>
</template>

<script setup>
import axios from "axios";
import { onBeforeMount, onMounted, ref } from "vue"
var posts = ref([])

onBeforeMount(async () => {
  var response = await axios.get("https://jsonplaceholder.typicode.com/posts")
  posts.value = response.data;
})




</script>