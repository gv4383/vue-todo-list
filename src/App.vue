<template>
  <div id="app">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <div class="main-container">
      <div class="title">
        <img alt="Vue logo" src="./assets/logo.png">
        <h1>Vue To-Do List</h1>
        <input v-model="userInput" placeholder="Type a new to-do" type="text">
        <button @click="addToList">Submit</button>
      </div>
      <main>
        <p :key="index" v-for="(item, index) in list" @click="removeFromList(index)">{{ item }}</p>
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
      userInput: "",
      list: ["Hello", "World!", "Click me to remove me from the list!"]
    };
  },
  methods: {
    addToList: function() {
      this.list.push(this.userInput);
      this.userInput = "";
    },
    removeFromList: function(i) {
      this.list.splice(i, 1);
    }
  },
  components: {
    HelloWorld
  }
};
</script>

<style lang="scss">
@import "./sass/main";
</style>
