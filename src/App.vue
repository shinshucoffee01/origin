<template>
  <middleSection/>
  <headerApp/>
  <testApp/>
</template>

<script>
//import middleSection from './components/middleSection.vue'
//import headerApp from './components/headerApp.vue'
import testApp from './components/testApp.vue'




export default {
  name: 'App',
  components: {
    //middleSection,
    //headerApp,
    testApp

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
