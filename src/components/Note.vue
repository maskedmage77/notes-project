<template>
<div class="contentWindow">
    <img class="x_image" src="../assets/images/x_grey.png" @click="deleteNote()">
    <h2>{{ title }}</h2>
        <div v-html="textContent">
        </div>
    </div>
</template>

<script>
export default {
    name: 'Note',
    props: ['title', 'textContent'],
    methods: {
        deleteNote() {
            this.$emit('deleteNote');
        }
    }
    
}
</script>

<style>
.contentWindow {
    color: grey;
    padding: 0.5em;
    padding-left: 1em;
    padding-right: 1em;
    margin: 0.5em;
    margin-top: 0em;
    margin-bottom: 2em;
    background: var(--innerWindow);
    border-radius: 0.5em;
    height: auto;
    filter: drop-shadow(0 0 10px var(--innerWindow));
    break-inside:avoid;
}
.contentWindow a {
    color: var(--accentColor)
}

.contentWindow h2 {
    color: white;
}

.x_image {
    width: 32px;
    position: absolute;
    right: 0.5em;
}

.x_image:hover {
    filter: invert(8%) sepia(200%) saturate(6012%) hue-rotate(4deg) brightness(60%) contrast(115%);
}
</style>