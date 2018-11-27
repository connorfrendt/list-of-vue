<template>
    <ul class="characters">
        <li v-for="character in characters"
            v-bind:class="{character: true, selected: character === selected }"
            v-bind:key="character.name"
            v-on:click="onSelect(character)">
            <img v-bind:src="character.image">
            <h3>{{character.name}} the {{character.role}}</h3>
        </li>
    </ul>
</template>

<script>
export default {
    props: {
        characters: Array,
        selected: Object,
        onSelect: Function
    }
};
</script>

<style>
.characters {
    display: flex;
    flex-wrap: wrap;
}

.character {
    list-style: none;
    position: relative;
    width: 200px;
    height: 200px;
    border: 1px solid #aaa;
    text-align: center;
    margin-right: 3px;
    cursor: pointer;
}

.character.selected {
    background: pink;
}

.character h3 {
    text-shadow: 1px 1px 1px white;
}
.character img {
    height: 70%;
    width: auto;
    position: absolute;
    bottom: 10px;
    left: 0;
    right: 0;
    margin: auto;
}
</style>