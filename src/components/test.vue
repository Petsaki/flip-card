<template>
      <div class="wrapper">
          <button @click="testFun">Front button</button>
        <transition  name="flip" mode="out-in" >
            <div class="card2" :key="opa1">
                    <h1 v-if="showFront" key="front" class="outer-front">hi</h1>
                    <h1 v-else key="back" class="outer-front">hi! Lorem ipsum dolor sit amet consectetur adipisicing elit. Quibusdam voluptatum at rerum ex iure ad, dolorem atque et pariatur dolore.</h1>    
            </div>
        </transition>
    </div>
</template>

<script>

export default {
    name: 'AppTest',
    data(){
        return{
            showFront: true,
            opa1:1,
            showBack:false,
        }
    },
    methods:{
        testFun(){
            this.opa1= this.opa1 + 1
            // if (this.showFront){
            //     setTimeout(()=>{
                    this.showBack = !this.showBack
            //     },"500")
            //     this.showFront=false;
            // }else{
            //     setTimeout(()=>{
                    this.showFront = !this.showFront
            //     },"500")
            //     this.showBack=false;
            // }
        }
    }
}
</script>

<style>
.wrapper{
    perspective: 1000px;
    transform-style: preserve-3d;
}

.card2{
    perspective: 1000px;
    transform-style: preserve-3d;
}
.outer-back,.outer-front {
    background-color: chartreuse;
    border-radius: .75rem;
}
.flip-enter{
    transform: rotateY(-90deg);
}
.flip-leave-to{
    transform: rotateY(90deg);
}
.flip-enter-to{
    transform: rotateY(0deg);
}
.flip-leave {
    transform: rotateY(0deg);
}

.flip-enter-active{
    transition-delay: .5s;
}
.flip-enter-active,
.flip-leave-active {
    transition: all .5s linear;
}
</style>