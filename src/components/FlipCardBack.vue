<template>
<div>
    <div class="flex-row-end">
        <button class="btn-x" @click="$parent.$emit('cardclicked')">✕</button>
    </div>
    <div class="flex-col">
        <h2>im the back</h2>
        <span>Lorem ipsum dolor sit amet consectetur adipisicing elit. Similique, nihil minima, assumenda quisquam doloribus consequuntur sunt sequi eaque incidunt, quaerat aliquam laborum possimus esse nisi consectetur nesciunt. Eos, explicabo vel.
        Distinctio fugit reprehenderit ipsum ipsam. Eum similique in rerum, sunt iusto, fugit, perspiciatis repudiandae dolore eveniet maxime inventore illo quibusdam. Deserunt nulla id quasi, neque nisi obcaecati sint et porro?</span>
    </div>

</div>
</template>

<script>
export default {

}
</script>

<style scoped>
.flex-col{
    position: relative;
    display: flex;
    flex-flow: column;
}

.flex-row-end{
    display: flex;
    justify-content: flex-end;
}
.btn-x{
    background-color: transparent;
    border: none;
    cursor: pointer;
    color: black;
    font-size: 1.2rem;
    padding: 0;
    margin: 0;
    line-height: .5rem;
}
</style>