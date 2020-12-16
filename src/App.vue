<template>

       <div id="app">
<!--
 
    <ComponentsBasics/>
    <InputBindings/>
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <Componenttwo value="helo two"/>
    <ConditionalRendering />
    <ListRendering/>
-->
  <ComponentsAd :propVal="value" :propVal2="value1"/>

  <input v-model="fname"/>
  <input v-model="lname"/>
  {{fname}}{{lname}}

  </div>
</template>

<script>
/*
import HelloWorld from './components/HelloWorld.vue'
import Componenttwo from './components/Componenttwo.vue'
import ConditionalRendering from './components/ConditionalRendering.vue'
import ListRendering from './components/ListRendering.vue'
import InputBindings from './components/InputBindings.vue'
import Componenttwo from './components/Componenttwo.vue'

import ComponentsBasics from './components/ComponentsBasics.vue'
*/
import ComponentsAd from './components/ComponentsAd'

export default {
  name: 'App',
  components: {
/*
    HelloWorld,
    Componenttwo,
    ConditionalRendering,
    ListRendering,
    InputBindings,
     ComponentsBasics
*/
ComponentsAd
   
  },
data:()=>{
  return({
    value: ["one","two","three","fout"],
    value1:{name:'chris',
    age:12,
    sex:'some'},
    fname:'chris',
    lname:'hellena'
   
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
