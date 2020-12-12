<template>
   <div>
       <!--Mustaches cannot be used inside HTML attributes. Instead, use a v-bind directive:
        example:  <div v-bind:id="dynamicId"></div>
        -->
       <h1>{{name}}</h1>
        <h2 @click="returnReverse">{{returnReverse(name)}} yo</h2>
       <p v-if="seen">yes you can see me</p>
   </div>
</template>

<script>


export default {
    data:()=>{
        return({
            name:"hero panti",
            seen:false,
            reversename:"name"
            })
    },methods:{
        returnReverse(a){
            console.log(a.split('').reverse().join(''))
            return (a.split('').reverse().join(''))
        }
    }
}
</script>