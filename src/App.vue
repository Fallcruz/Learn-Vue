<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <TimePage/>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import TimePage from './components/TimePage.vue'

export default {
  name: 'App',
  components: {
    TimePage
  }
}
</script>

<style>
/* #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */
@import url('https://fonts.googleapis.com/css2?family=Rubik:wght@400;500&display=swap');
* {
  margin: 0 !important;
  padding: 0 !important;
  box-sizing: border-box;
}
</style>
