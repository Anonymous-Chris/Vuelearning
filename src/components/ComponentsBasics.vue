<template>
    <div >
        <h1>Component Basics</h1>
        <button v-on:click="increment">You clicked me {{count}} times</button>
    </div>
</template>

<script>
export default {
    data:()=>{
        return ({
            count:0
        })
    },
    methods:{
        increment(){
            return this.count++
        }
    }
}
</script>

<style>

</style>