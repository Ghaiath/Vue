<template>
  <br><br>
  <input v-model="form.userId" type="text" placeholder="userId">
  <br>
  <input v-model="form.title" type="text" placeholder="title">
  <br>
  <input v-model="form.body" type="text" placeholder="body">
  <br><br>
  <button @click="CreatePost">Create a Post</button>
  <br><br>
  <h3>{{ post.userId }}</h3>
  <h3>{{ post.title }}</h3>
  <h3>{{ post.body }}</h3>
</template>

<script setup>
import axios from 'axios';
import { ref } from 'vue';
var form = ref({
  userId: "",
  title: "",
  body: ""
})

var post = ref({
  userId: "",
  title: "",
  body: ""
});

var CreatePost = async () => {
  var response = await axios.post("https://jsonplaceholder.typicode.com/posts", form.value)
  post.value = response.data
  console.log(response.data);

}



</script>