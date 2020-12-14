<template>
    <div >
        <h1>Form Input Bindings</h1>
        <label>Name</label>
        <input v-model="input"/>
        {{input}}
        <br/>
        <label>Checkbox</label>
        <input type="checkbox" id="checkbox" v-model="checked"/>

        {{checked}}

        <br/>
        <input type="checkbox" id="jack" value="Jack" v-model="checkedNames" />
        <label for="jack">Jack</label>
        <input type="checkbox" id="john" value="John" v-model="checkedNames" />
        <label for="john">John</label>
        <input type="checkbox" id="mike" value="Mike" v-model="checkedNames" />
        <label for="mike">Mike</label>

        <h1>Checked multiple values</h1>
        {{checkedNames}}

        <br/>
        <h1>Radio buttons</h1>
        <input type="radio" id="one" value="One" v-model="picked" />
        <label for="one">One</label>
        <br />
        <input type="radio" id="two" value="Two" v-model="picked" />
        <label for="two">Two</label>

        <p>Chosen radio button:</p>{{picked}}
        <br/>

        <select v-model="selected">
        <option disabled value="">Please select one</option>
        <option>A</option>
        <option>B</option>
        <option>C</option>
        </select>

       <p>Selected button:</p>{{selected}}

       <br/>

        <h1>Dynamic binding of values</h1>
        <input type="radio" v-model="pick" v-bind:value="a" />
        <p>Pick: </p>{{pick}}
    </div>
</template>

<script>
export default {
    data:()=>{
        return ({
            input:'kalyan',
            checked:false,
            checkedNames:[],
            picked:'One',
            selected: '',
            pick:'',

            a:1111
        })
    },
    methods:{
     
    }
}
</script>

<style>

</style>