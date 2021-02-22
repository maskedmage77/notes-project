<template>
    <div class="mainWindow">       
        <Note v-for="note in notes" v-bind:key='note.title' :title='note.title' :textContent='note.textContent' @deleteNote="deleteNote(note)"></Note>
    </div>
</template>

<script>
import Note from './Note.vue'

export default {
    name: 'NoteContainer',
    components: {
        Note
    },
    data() {
        return {
            notes: [
                {'title':'first asdddsa2titme', 'textContent':'<p>Pariatur irure sit amet incididunt. Voluptate dolore fugiat ea consectetur est est voluptate id ut duis duis do. Incididunt et ad consectetur aute eu eu irure laboris sunt fugiat incididunt ex. Lorem ad duis do sit deserunt laboris excepteur eiusmod velit est.</p>'},
                {'title':'secondasd title', 'textContent':'<p>random text 2</p><p>random text 2</p><p>random text 2</p>'},
                {'title':'randoasdmM!', 'textContent':'<p>Minim sit in nisi adipisicing ipsum consequat dolore deserunt id.</p>'},
                {'title':'sec41ond title', 'textContent':'<p>random text 2</p><p>random text 2</p><p>random text 2</p>'},
            {'title':'first ti4tme', 'textContent':'<p>Non aliqua velit laboris nulla cupidatat labore do amet. Elit consectetur sunt velit magna commodo fugiat mollit aliqua velit ad dolore do eiusmod. Elit laborum ipsum nisi laboris quis est nostrud non. Mollit qui cupidatat laboris Lorem proident sit commodo.</p>'},
                {'title':'seco12nd title', 'textContent':'<p>random text 2</p><p>random text 2</p><p>random text 2</p>'},
                {'title':'sec231ond title', 'textContent':'<p>random text 2</p><p>random text 2</p><p>random text 2</p>'},
            ]
        }
    },
    methods: {
      deleteNote(note) {
        this.notes.splice(this.notes.indexOf(note), 1);
        //remove one element starting from the element 'fruit'
      }
    }
}
</script>

<style>
.mainWindow {
    margin-top: 2em;
    column-count: 3;
    column-gap: 1rem;
    display: block;
}
</style>