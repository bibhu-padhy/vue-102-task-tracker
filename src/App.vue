<template>
  <div class="main_container">
    <Header title="Task Tracker!" />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
export default {
  name: "App",
  components: {
    Header,
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
.main_container {
  margin: auto;
  width: 500px;
  min-height: 400px;
  border: 1px solid saddlebrown;
  padding: 10px;
}
</style>
