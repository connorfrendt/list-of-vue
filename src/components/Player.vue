<template>
    <section>
        <div v-if="character">
            <h2>{{character.name}}</h2>
            <p>{{character.name}} the {{character.role}}</p>
            <img v-bind:src="character.img" style="height: 500px">
        </div>
        <div v-else><u>Please choose a character for your player</u></div>
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
img {
    height: 500px;
}
</style>