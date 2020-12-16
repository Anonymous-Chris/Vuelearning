<template>
    <div >
        <h1>Components In Depth </h1>
       <li v-for="p in propVal" v-bind:key="p.id">
           {{p.id}} {{p}}
       </li>

       <li>
           <p>object</p>   
                   {{propVal2.name}}
       </li>
    </div>
</template>

<script>
export default {
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