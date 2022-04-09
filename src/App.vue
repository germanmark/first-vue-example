<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <PageHeader greeting="Welcome" :myNum="8"/> <!-- Usage -->
    <PageFooter/>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import PageHeader from './components/PageHeader.vue' //Import
import PageFooter from './components/PageFooter.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld
    PageHeader, //Registration
    PageFooter
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
  background-color: bisque;
}
div{
  background-color: bisque;
}
*{
  background-color: bisque;
}
</style>
