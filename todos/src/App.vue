<template>
  <div id="app">
    <img alt="React logo" src="./assets/react-2.svg">
    <HelloWorld msg="This is a prop"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
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
img {
  height: 200px;
  width: 200px;
  animation-name: rotate-logo;
  animation-duration: 4s;
  animation-iteration-count: infinite;
  animation-timing-function: linear;
}

@keyframes rotate-logo {
  0% {transform: rotate(0deg)}
  100% {transform: rotate(360deg)}
}
</style>
