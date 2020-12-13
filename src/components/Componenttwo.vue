<template>
<div class="menu">

<button v-on:click="increment">Click to increment</button>
<p>{{counter}}</p>
<p>{{author.books[0]}}</p>
<p>No of books written by {{author.name}} is: {{noofBooks}}</p>
<!--the data can be accessed in the form of objects as well in the template -->
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
             author:{
                 name:'kshitij',
                 books:[
                     'hero panti',
                     'maya nai maya',
                     'phul maya',
                     'christina'
                 ]
             }
            })
    },methods:{
        increment(){
            return this.counter+=1;
        }
    },computed:{
        noofBooks(){
            return this.author.books.length
        }
    }

    }

</script>


<style scoped>
   div.menu div.active{
        color:green
    }
</style>