<template>
<div>
    <div >
        <h1>Components In Depth </h1>
       <li v-for="p in propVal" v-bind:key="p.id">
          {{p}}
       </li>

       <li>
           <p>object</p>   
                   {{propVal2.name}}
       </li>
    </div>
    <h1>Another component has been injected here inside ComponentsAd to test PROVIDE AND INJECT</h1>
    <p>PROVIDE AND INJECT  are not reactive ny default. we need to provide computed property</p>
    <HelloWorld/>
    </div>
</template>

<script>
import HelloWorld from './HelloWorld.vue'

export default {
    components:{
        HelloWorld
    },
    data:()=>{
        return ({

        })
    },
    props:{
        propVal:[],
        propVal2:{}
    },
    methods:{
     
    }
}
</script>

<style>

</style>