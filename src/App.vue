<template>
  <div id="app">
    <myform/>
  </div>
</template>

<script>
import myform from './components/myform.vue'

export default {
  name: 'app',
  components: {
    myform
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
