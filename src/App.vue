<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <h1>Vue To-Do List</h1>
    <main>
      <p :key="item" v-for="item in list">{{ item }}</p>
    </main>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "app",
  data() {
    return {
      list: ["Hello", "World"]
    };
  },
  components: {
    HelloWorld
  }
};
</script>

<style lang="scss">
@import "./sass/main";
</style>
