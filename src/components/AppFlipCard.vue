<template>
    <div class="wrapper">
        <transition :name="cardTransition" mode="out-in">
                <div v-if="!showFront" key="back" class="card">
                    <slot name="back">Default back</slot>
                </div>
                <div v-else class="card" key="front">
                    <slot name="front" >Default front</slot>
                </div>
        </transition>
    </div>
</template>

<script>
export default {
    name: 'AppFlipCard',
    data(){
        return{
            showFront:true,
            flipFront:true,
        }
    },
    computed:{
        cardTransition(){
            return this.flipFront ? 'flip-front' : 'flip-back'
        }
    },
    methods:{
        cardOnClick(){
            this.showFront = !this.showFront
            this.flipFront = !this.flipFront

        }
    },
    created() {
        this.$on('cardclicked', this.cardOnClick)
    },
}
</script>

<style>

.wrapper{
    perspective: 1000px;
}

.card {
    background-color: chartreuse;
    border-radius: .75rem;
    padding: .5rem;
}

.flip-front-enter,
.flip-back-leave-to{
    transform: rotateY(90deg);
}
.flip-front-leave-to,
.flip-back-enter {
    transform: rotateY(-90deg);
}

.flip-front-enter-active,
.flip-front-leave-active,
.flip-back-enter-active,
.flip-back-leave-active {
    transition: all .4s linear;
}

</style>