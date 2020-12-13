<template>
<div class="menu">
   <div v-bind:class="{active:isActive,'text-danger': hasError }">
       <!--Mustaches cannot be used inside HTML attributes. Instead, use a v-bind directive:
        example:  <div v-bind:id="dynamicId"></div>
        -->
       <h1>{{name}}</h1>

        <h2 @click="returnReverse(name)">{{returnReverse(name)}} yo</h2>
       <p v-if="seen">yes you can see me</p>
   </div>
<!-- v-model is used for two way binding. It means if one of the value changes ,
both the values are changed. -->
   <input v-model="counter">
    <h1>{{counter}}</h1>

    <div>
        <ol>
            <li v-for="todo in todos" v-bind:key="todo.text">
                {{todo.text}}
            </li>
        </ol>
    </div>
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

            name:"hero panti",
            seen:false,
            reversename:"name",
            isActive:false,
             hasError: true,
             counter:0,
                   todos: [
        { text: 'Learn JavaScript' },
        { text: 'Learn Vue' },
        { text: 'Build something awesome' }
      ]
            })
    },methods:{
        returnReverse(a){
         //   console.log(a.split('').reverse().join(''))
           // console.log(this.seen)
            return (a.split('').reverse().join(''))
    
        }
    },
    mounted(){
        setInterval(()=>{
            this.counter++
            //console.log(this.name)
        },1000)
    }
}
</script>


<style scoped>
   div.menu div.active{
        color:green
    }
</style>