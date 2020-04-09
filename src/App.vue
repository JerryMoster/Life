<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <life />
  </div>
</template>

<script>
import Life from './components/Life'
export default {
  name: 'App',
  components: {
    Life
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
