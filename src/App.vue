<template>
  <div>
    <Demo />
    <Box />
    <Books />
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import Demo from "./components/Demo.vue";
import Box from "./components/Box.vue";
import Books from "./components/Books.vue";

export default {
  name: "App",
  components: {
    Demo,
    Box,
    Books,
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
  list-style: none;
}
</style>
