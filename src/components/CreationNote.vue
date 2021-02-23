<template>
    <div class="contentWindow" @mouseover="showControls = true" @mouseleave="showControls = false">
        <img class="x_image" src="../assets/images/x_grey.png" @click="this.$emit('showNewNote')">
        <form @submit.prevent="createNote()">
            <input placeholder="Title..." required v-model="title" />
            <textarea placeholder="Body..." required v-model="body" />
            <button>Save Note</button>
        </form>
    </div>
</template>

<script>
export default {
    name: 'CreationNote',
    data() {
        return {
            title: '',
            body: ''
        }
    },
    methods: {
        createNote() {
           this.$emit('createNote', this.title, this.body)
        }
    }
}
</script>

<style>

form {
    padding: 0em;
    
}
input,textarea {
    font-family: 'Josefin Sans', sans-serif;
    background-color: inherit;
    border: none;
    border-radius: 0.5em;
    color: white;
    padding: 1em;
    padding-left: 0em;
    outline: none;
    font-size: 1em;
    display: block;
    width: 100%;
}
textarea {
    padding-top: 0em;
    resize: vertical;
}
input:first-of-type {
    font-size: 1.5em;
    font-weight: bold;
}
button {
    font-family: 'Josefin Sans', sans-serif;
    color: white;
    font-size: 1em;
    width: 100%;
    background-color: var(--accentColor);
    padding: 0.5em;
    border: 0px;
    border-radius: 0.5em;
    box-sizing: border-box;
    -webkit-appearance: none;
    outline: none;
    margin-bottom: 0.5em;
}
input:required,textarea:required {
    box-shadow:none;
}
input:invalid,,textarea:invalid {
    box-shadow:none;
}
</style>