<template>
  <button @click="GetPostList">Get all posts</button>
  <div v-for="post in posts" :key="post.id">
    <h3>{{ post.userId }}</h3>
    <h4>{{ post.title }}</h4>
    <h5>{{ post.body }}</h5>
    <hr>
  </div>
</template>

<script setup>
import axios from "axios";
import { ref } from "vue"
var posts = ref([])

var GetPostList = async () => {
  var response = await axios.get("https://jsonplaceholder.typicode.com/posts")
  posts.value = response.data;
  console.log(response.data);
}




</script>