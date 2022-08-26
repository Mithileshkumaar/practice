<template>
  <div>
    <h1>{{ name }}</h1>
    <button @click="setName()"></button>
  </div>
</template>

<script>
export default {
  name: "data",
  data() {
    return {
      name: "tony stank",
    };
  },
  methods: {
    setName() {
      this.name = "steve rogers";
    },
  },
};
</script>

<style scoped>
</style>