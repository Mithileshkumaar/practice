<template>
  <div>
    <form @submit.prevent="CreatePost">
      <label for="userId">user id</label>
      <input type="text" v-model="FormData.userId" />
      <label for="title">title</label>
      <input type="text" v-model="FormData.title" />
      <label for="body">body</label>
      <input type="text" v-model="FormData.body" />
      <button>create post</button>
    </form>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "CreatePost",
  data() {
    return {
      FormData: {
        userId: "",
        title: "",
        body: "",
      },
    };
  },
  methods: {
    CreatePost() {
      axios
        .post("https://jsonplaceholder.typicode.com/posts", this.FormData)
        .then((response) => {
          console.log(response.data);
        })
        .catch((error) => console.log(error));
    },
  },
};
</script>

<style scoped>
</style>