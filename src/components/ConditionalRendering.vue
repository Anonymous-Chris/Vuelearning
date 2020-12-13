<template >
<div>
<div v-if="number===2">
    <h1>Hello conditional rendering</h1>
    <div v-if="active">
    
    <canvas :style="{height:50 +'px',backgroundColor:'gray',width:50+'px',marginRight: 5 +'px'}"/>
    <canvas :style="{height:50 +'px',backgroundColor:'gray',width:50+'px'}"/>
    </div>
<div v-else><p>no it is false</p></div>
</div>

<div v-else-if="number===4">
    <h1>Hello conditional rendering</h1>
    <div v-if="active">

    <canvas :style="{height:50 +'px',backgroundColor:'gray',width:50+'px',marginRight: 5 +'px'}"/>
    <canvas :style="{height:50 +'px',backgroundColor:'gray',width:50+'px',marginRight: 5 +'px'}"/>
    <canvas :style="{height:50 +'px',backgroundColor:'gray',width:50+'px',marginRight: 5 +'px'}"/>
    <canvas :style="{height:50 +'px',backgroundColor:'gray',width:50+'px',marginRight: 5 +'px'}"/>

    </div>
<div v-else><p>no it is false</p></div>
</div>

<div v-else-if="number===6">
    <h1>Hello conditional rendering</h1>
    <div v-if="active">

    <canvas :style="{height:50 +'px',backgroundColor:'gray',width:50+'px',marginRight: 5 +'px'}"/>
    <canvas :style="{height:50 +'px',backgroundColor:'gray',width:50+'px',marginRight: 5 +'px'}"/>
    <canvas :style="{height:50 +'px',backgroundColor:'gray',width:50+'px',marginRight: 5 +'px'}"/>
    <canvas :style="{height:50 +'px',backgroundColor:'gray',width:50+'px',marginRight: 5 +'px'}"/>
    <canvas :style="{height:50 +'px',backgroundColor:'gray',width:50+'px',marginRight: 5 +'px'}"/>
    <canvas :style="{height:50 +'px',backgroundColor:'gray',width:50+'px',marginRight: 5 +'px'}"/>
    </div>
<div v-else><p>no it is false</p></div>
</div>

<div v-else-if="number===9">
    <h1>Hello conditional rendering</h1>
    <div v-if="active">

    <canvas :style="{height:50 +'px',backgroundColor:'gray',width:50+'px',marginRight: 5 +'px'}"/>
    <canvas :style="{height:50 +'px',backgroundColor:'gray',width:50+'px',marginRight: 5 +'px'}"/>
    <canvas :style="{height:50 +'px',backgroundColor:'gray',width:50+'px',marginRight: 5 +'px'}"/>
    <canvas :style="{height:50 +'px',backgroundColor:'gray',width:50+'px',marginRight: 5 +'px'}"/>
    <canvas :style="{height:50 +'px',backgroundColor:'gray',width:50+'px',marginRight: 5 +'px'}"/>
    <canvas :style="{height:50 +'px',backgroundColor:'gray',width:50+'px',marginRight: 5 +'px'}"/>
    <canvas :style="{height:50 +'px',backgroundColor:'gray',width:50+'px',marginRight: 5 +'px'}"/>
    <canvas :style="{height:50 +'px',backgroundColor:'gray',width:50+'px',marginRight: 5 +'px'}"/>
    <canvas :style="{height:50 +'px',backgroundColor:'gray',width:50+'px',marginRight: 5 +'px'}"/>
    </div>
<div v-else><p>no it is false</p></div>
</div>

</div>
</template>



<script>
export default {
    data: ()=>{
        return({
      number:2, //change this number to change the number of canvas displayed
      active:true
        })
        
    }
}
</script>