<template>
    <div >
        <h1>Transitions</h1>
        <div class="circle"> 
</div>


<div>
      <button @click="show = !show">Toggle show</button>
  <transition name="bounce">
    <p v-if="show">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Mauris facilisis
      enim libero, at lacinia diam fermentum id. Pellentesque habitant morbi
      tristique senectus et netus.
    </p>
  </transition>
</div>


<!--Cool stuff from here-->
<div id="animated-number-demo">
  <input v-model.number="number" type="number" step="20" />
  <p>{{ animatedNumber }}</p>
</div>

    </div>
</template>

<script>
import {gsap} from "gsap";

export default {
    data:()=>{
        return ({   
            show: true,
            number: 0,
            tweenedNumber: 0
        })
    },
    methods:{
     
    },
    mounted:function(){
          gsap.to('.circle', {x: 500,ease: 'bounce.out', duration: 3,y:-100})
    },
    computed: {
        animatedNumber() {
        return this.tweenedNumber.toFixed(0)
    }
    },
    watch: {
        number(newValue) {
        gsap.to(this.$data, { duration: 0.5, tweenedNumber: newValue })
    }
    }
}
</script>

<style>

/* cool stuff styling*/


/*ends cool */
    div{
  margin-top: 10em
}

.circle{
  background-color:red;
  height: 5em;
  width: 5em;
  border-radius: 100%
}


.bounce-enter-active {
  animation: bounce-in 0.5s;
}
.bounce-leave-active {
  animation: bounce-in 0.5s reverse;
}
@keyframes bounce-in {
  0% {
    transform: scale(0);
  }
  50% {
    transform: scale(1.25);
  }
  100% {
    transform: scale(1);
  }
}
</style>