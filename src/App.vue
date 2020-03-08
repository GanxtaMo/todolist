<template>
  <div id="app">
    <todo>

    </todo>

  </div>
</template>

<script>
import todo from "./components/to_do.vue"
export default {
  name: 'App',
  components: {
    todo,
    
  }
}
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
