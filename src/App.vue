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
 <DynamicAsyncComponents />


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
import ComponentsAd from './components/ComponentsAd'
*/

import DynamicAsyncComponents from './components/DynamicAsyncComponents'
export default {
  name: 'App',
  components: {
/*
    HelloWorld,
    Componenttwo,
    ConditionalRendering,
    ListRendering,
    InputBindings,
     ComponentsBasics,
     ComponentsAd,
*/

DynamicAsyncComponents
   
  },

  //PROVIDE HERE IN PARENT COMPONENT. INJECT IN HELLOWORLD.VUE THE CHILD COMPONENT

data:()=>{
  return({
    value: ["one","two","three","fout"],
    value1:{name:'chris',
    age:12,
    sex:'some'},
    fname:'chris',
    lname:'hellena'
   
  })
},
  provide(){
    return({
      length: this.fname.length
    })
  },
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
