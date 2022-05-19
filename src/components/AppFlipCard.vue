<template>
    <div class="wrapper">

        <transition-group tag="div" name="flip2" mode="out-in" class="card">
                <div v-if="showBack" key="back" class="outer-back">
                    <slot name="back">Default back</slot>
                </div>
                <div v-if="showFront" class="outer-front" key="front">
                    <slot name="front" >Default front</slot>
                </div>
        </transition-group>
    </div>
</template>

<script>
export default {
    name: 'AppFlipCard',
    data(){
        return{
            opa:1,
            showFront:true,
            showBack:false,
        }
    },
    methods:{
        test(){

    
            if (this.opa === 1){
                this.opa=0
            }else{
                this.opa=1
            }

            setTimeout(()=>{
                this.showFront = !this.showFront
            },"500")
        }
    },
    created() {
        this.$on('cardclicked', this.test)
    },
}
</script>

<style>

.wrapper{
    perspective: 1000px;
    transform-style: preserve-3d;
}
.card {
    background-color: chartreuse;
    border-radius: .75rem;
    position: relative;
}


.card > * {
    backface-visibility: hidden;
    background-color: chartreuse;
    border-radius: .75rem;
    padding: .5rem;
    position: relative;
    width: 100%;
    height: 100%;
    box-sizing: border-box;
}

.flip2-enter,
.flip2-leave-to{
    transform: rotateY(90deg);
}
.flip2-enter-to,
.flip2-leave {
    transform: rotateY(0deg);
}

.flip2-enter-active,
.flip2-leave-active {
    transition: all 1s linear;
}
</style>