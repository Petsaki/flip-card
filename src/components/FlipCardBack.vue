<template>
    <div>
        <span>im the back</span>
        <span>Lorem ipsum dolor sit amet consectetur adipisicing elit. Similique, nihil minima, assumenda quisquam doloribus consequuntur sunt sequi eaque incidunt, quaerat aliquam laborum possimus esse nisi consectetur nesciunt. Eos, explicabo vel.
        Distinctio fugit reprehenderit ipsum ipsam. Eum similique in rerum, sunt iusto, fugit, perspiciatis repudiandae dolore eveniet maxime inventore illo quibusdam. Deserunt nulla id quasi, neque nisi obcaecati sint et porro?</span>
        <button id="back" @click="$parent.$emit('cardclicked',$event.target.id)">back button</button>
    </div>
</template>

<script>
export default {

}
</script>

<style>

</style>