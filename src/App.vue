
<template>
  <div></div>
  <!-- <PostList />
  <CreatePost /> -->
  <Data />
</template>


<script>
// import PostList from "./components/PostList.vue";
// import CreatePost from "./components/CreatePost.vue";
import Data from "./components/data.vue";

export default {
  name: "App",

  components: { Data },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
