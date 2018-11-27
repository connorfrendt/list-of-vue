<template>
    <section>
        <div v-if="character">
            <h2>{{character.name}}</h2>
            <p>{{character.name}} the {{character.role}}</p>
            <img v-bind:src="character.image">
        </div>
        <div v-else>Please choose a character for your player</div>
    </section>
</template>

<script>
export default {
    props: {
        character: Object,
    }
};
</script>

<style>

</style>