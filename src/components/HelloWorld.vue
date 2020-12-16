<template>
<div>

      <h3>
    <li v-for="m in msg" v-bind:key="m.name">
      <p>{{m.name}}   {{m.country}}</p><br/>
    </li>
  </h3>
<div>



  <div  @click="dialogIsOpen=true" class="hello">
    <h1> Create a dialog box </h1>


  </div>
  
     
    <dialog :open="dialogIsOpen">
   <h3>{{msg}}</h3>
        <button @click="dialogIsOpen=false">Close</button>
    </dialog>
</div>
</div>
</template>

<script>
if(!localStorage.getItem("valueInput")){


localStorage.setItem("valueInput",1)
}
export default {
  name: 'HelloWorld',
  props: {
    msg: []
  },
  data: function(){
    return{
      dialogIsOpen:false,
      value:localStorage.getItem("valueInput"),
      rawHtml:"hello there boy"
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>