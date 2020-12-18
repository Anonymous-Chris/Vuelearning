<template>
    <div >
        Dynamic and Async Components
    <button @click="currentTab===tab" v-for="tab in tabs" v-bind:key="tab" :class="['tab-button',{active:currentTab===tab}]">{{tab}}</button>
     <div>
    <h2>Hello this is for refs man!</h2>
    <p>You have counted {{this.counter}} times</p>
    <input type="text" ref="input">
    <button @click="submit">Add 1 to counter</button>
  </div>
    </div>
</template>

<script>
export default {
    data:()=>{
        return ({
            currentTab: 'Home',
            tabs:['Home','Posts','Archive'],
            counter:0
        })
    },
    methods:{
     submit(){
         this.counter++
         console.log(this.$refs)
         console.log(this.$refs.input.value)
        
     }
    }
}
</script>

<style>

</style>

