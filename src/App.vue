<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <div>11111233456677</div>
    <el-button type="primary">Button</el-button>
    <el-button type="primary">绷不住啦</el-button>
  </div>
</template>

<script>
import Monitor from 'website-monitoring'
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  mounted() {
    Monitor.resource.init((data) => {
      console.log(data)
    })
    Monitor.perf.init((data) => {
      console.log(data)
    })
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
