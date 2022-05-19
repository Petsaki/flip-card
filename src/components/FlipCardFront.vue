<template>
    <div>
        <span>im the front</span>
        <button id="front" @click="$parent.$emit('cardclicked',$event.target.id)">Front button</button>
    </div>
</template>

<script>
export default {

}
</script>

<style>

</style>