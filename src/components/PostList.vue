<template>
  <div>
    <button @click="getposts">load post</button>
    <div v-for="post in posts" :key="post.id">
      <h3>{{ post.id }}</h3>
      <h5>{{ post.title }}</h5>
      <p>{{ post.body }}</p>
    </div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "PostList",
  data() {
    return {
      posts: [],
    };
  },
  methods: {
    getposts() {
      axios
        .get("https://jsonplaceholder.typicode.com/posts")
        .then((response) => {
          console.log(response.data);
          this.posts = response.data;
        })
        .catch();
    },
  },
};
</script>

<style scoped>
</style>