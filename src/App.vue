<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">

    <InputBindings/>

    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <Componenttwo value="helo two"/>
    <ConditionalRendering />
    <ListRendering/>

  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Componenttwo from './components/Componenttwo.vue'
import ConditionalRendering from './components/ConditionalRendering.vue'
import ListRendering from './components/ListRendering.vue'
import InputBindings from './components/InputBindings.vue'

//import Componenttwo from './components/Componenttwo.vue'
export default {
  name: 'App',
  components: {
    HelloWorld,
    Componenttwo,
    ConditionalRendering,
    ListRendering,
    InputBindings
   
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