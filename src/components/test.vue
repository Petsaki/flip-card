<template>
      <div class="wrapper">
          <button @click="testFun">Front button</button>
        <transition  :name="cardTransition" mode="out-in" >
                    <h1 v-if="showFront" key="front" class="card">hi</h1>
                    <h1 v-else key="back" class="card">hi! Lorem ipsum dolor sit amet consectetur adipisicing elit. Quibusdam voluptatum at rerum ex iure ad, dolorem atque et pariatur dolore.</h1>    
        </transition>
    </div>
</template>

<script>

export default {
    name: 'AppTest',
    data(){
        return{
            showFront: true,
            flipFront: true,
        }
    },
    computed:{
        cardTransition(){
            return this.flipFront ? 'flip-front' : 'flip-back'
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
            setTimeout(()=>{
                this.flipFront = !this.flipFront
            },'500')

           
        }
    }
}
</script>

<style>

</style>