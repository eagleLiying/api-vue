<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <br />
    <p v-show="seen">现在你看到我了</p>
    <button @click="click">{{ seen ? "点击我隐藏" :"点击我显示" }}</button>
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "app",
  components: {
    HelloWorld
  },
  data: function() {
    return {
      seen: true
    };
  },
  methods: {
    click: function() {
        this.seen = !this.seen;
    }
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
