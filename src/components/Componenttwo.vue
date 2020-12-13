<template>
<div class="menu">

<button v-on:click="increment">Click to increment</button>
<p>{{counter}}</p>
</div>
</template>

<script>


export default {
    name:'Componenttwo',
    props:{
        value: String
    },
    data:()=>{
        return({
             counter:0,
            })
    },methods:{
        increment(){
            return this.counter+=1;
        }
    },

    }

</script>


<style scoped>
   div.menu div.active{
        color:green
    }
</style>