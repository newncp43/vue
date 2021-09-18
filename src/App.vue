<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <faculty />
    <testna />
    
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import faculty from "./components/faculty.vue";
import Testna from './components/Testna.vue';


export default {
  name: "App",
  components: {
    HelloWorld,
    faculty,
    Testna

  },
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
