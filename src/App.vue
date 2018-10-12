<template>
  <div id="app">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <div class="main-container">
      <div class="title">
        <img alt="Vue logo" src="./assets/logo.png">
        <h1>Vue To-Do List</h1>
        <input placeholder="Type a new to-do">
        <button>Submit</button>
      </div>
      <main>
        <p :key="index" v-for="(item, index) in list">{{ item }}</p>
      </main>
    </div>
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
