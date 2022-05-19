<template>
<div>
    <div class="flex-row-between">
        <h2 class="block-inline">im the back</h2>
        <button class="btn-x" @click="$parent.$emit('cardclicked')">✕</button>
    </div>
    <span>Lorem ipsum dolor sit amet consectetur adipisicing elit. Similique, nihil minima, assumenda quisquam doloribus consequuntur sunt sequi eaque incidunt, quaerat aliquam laborum possimus esse nisi consectetur nesciunt. Eos, explicabo vel.
    Distinctio fugit reprehenderit ipsum ipsam. Eum similique in rerum, sunt iusto, fugit, perspiciatis repudiandae dolore eveniet maxime inventore illo quibusdam. Deserunt nulla id quasi, neque nisi obcaecati sint et porro?</span>

</div>
</template>

<script>
export default {

}
</script>

<style scoped>

.block-inline{
    display: inline-block;
}

.flex-row-between{
    padding: 0 .75rem;
    box-sizing: border-box;
    display: flex;
    justify-content: space-between;
    width: 100%;
}
.btn-x{
    background-color: transparent;
    border: none;
    cursor: pointer;
    color: black;
    font-size: 1.2rem;
    padding: 0;
    margin: 0;
    line-height: 1rem;
}
</style>