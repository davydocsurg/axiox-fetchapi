<template>
  <div id="app">
  <h1>Ajax Requests with axios</h1>
    <ShowUsers/>
  </div>
</template>

<script>
import ShowUsers from './components/ShowUsers.vue'

export default {
  name: 'App',
  components: {
    ShowUsers
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
