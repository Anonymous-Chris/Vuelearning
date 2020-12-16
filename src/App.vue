<template>
  <div id="app">
    <ComponentsBasics/>
    
<!--
    <InputBindings/>
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <Componenttwo value="helo two"/>
    <ConditionalRendering />
    <ListRendering/>
-->
<HelloWorld :msg="artists"/>

<div>
  <li v-for="artist in artists" v-bind:key="artist.name">
    {{artist.name}}
  </li>
</div>

  </div>
</template>

<script>

import HelloWorld from './components/HelloWorld.vue'
/*
import Componenttwo from './components/Componenttwo.vue'
import ConditionalRendering from './components/ConditionalRendering.vue'
import ListRendering from './components/ListRendering.vue'
import InputBindings from './components/InputBindings.vue'
import Componenttwo from './components/Componenttwo.vue'
*/
import ComponentsBasics from './components/ComponentsBasics.vue'
export default {
  name: 'App',
  components: {

    HelloWorld,
    /*
    Componenttwo,
    ConditionalRendering,
    ListRendering,
    InputBindings
*/

    ComponentsBasics
  },
  data:()=>{
    return({
            artists: [
       {name: 'Davido', genre: 'afrobeats', country: 'Nigeria'},
       {name: 'Burna Boy', genre: 'afrobeats', country: 'Nigeria'},
       {name: 'AKA', genre: 'hiphop', country: 'South-Africa'},
       {name: 'Sarkodie', genre: 'hiphop', country: 'Ghana'},
       {name: 'Stormzy', genre: 'hiphop', country: 'United Kingdom'},
       {name: 'Lil Nas', genre: 'Country', country: 'United States'},
       {name: 'Nasty C', genre: 'hiphop', country: 'South-Africa'},
       {name: 'Shatta-walle', genre: 'Reagae', country: 'Ghana'},
       {name: 'Khalid', genre: 'pop', country: 'United States'},
       {name: 'ed-Sheeran', genre: 'pop', country: 'United Kingdom'}
      ]
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
