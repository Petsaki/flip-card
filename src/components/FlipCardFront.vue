<template>
    <div class="flex-col">
        <h2>im the front</h2>
        <button class="btn" id="front" @click="$parent.$emit('cardclicked')">Front button</button>
    </div>
</template>

<script>
export default {

}
</script>

<style scoped>

.flex-col{
    display: flex;
    flex-flow: column;
    align-items: center;
}

.btn{
    width: fit-content;
}
</style>
