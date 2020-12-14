<template>
    <div >
        <h1>list rendering</h1>
        <ul v-for="value in numbers" v-bind:key="value">
            
              <li v-for="x in evenNumbers(value)" v-bind:key="x">
                  {{x}}
              </li>
        </ul>
      
    </div>
</template>
<script>
export default {
    data:()=>{
        return ({
numbers:[[1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20],[21,22,23,24,25,26,272,28,29,211]]
        })
    },
    methods:{
        evenNumbers(value){
            return value.filter(value=>value%2===0)
        }
    }
}
</script>