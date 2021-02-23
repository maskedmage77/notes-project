<template>
    <div class="mainWindow">       
        <Note v-for="note in notes" v-bind:key='note.title' :title='note.title' :textContent='note.textContent' @deleteNote="deleteNote(note)"></Note>
        <CreationNote @createNote="createNote" @showNewNote="toggleShowNewNote()" v-if="showNewNote" />
    </div>
</template>

<script>
import Note from './Note.vue'
import CreationNote from './CreationNote.vue'

export default {
    name: 'NoteContainer',
    components: {
        Note,
        CreationNote
    },
    data() {
        return {
            notes: [
                {'title':'test object','textContent':'<p>Example Text</p>'}
            ],
            showNewNote: true
        }
    },
    methods: {
      deleteNote(note) {
        this.notes.splice(this.notes.indexOf(note), 1);
      },
      createNote(title,body) {
        let newNote = {title, textContent: '<p>' + body + '</p>'}
        this.notes.push(newNote);
      },
     toggleShowNewNote() {
        console.log('test');
        this.showNewNote = !this.showNewNote
      }
    },
    mounted() {
        if (localStorage.notes) {
        this.notes = JSON.parse(localStorage.getItem("notes") || "[]");
        }
    },
    watch: {
        notes: {
            deep: true,
            handler() {
                localStorage.setItem("notes", JSON.stringify(this.notes));
            }
        }
    }
}
</script>

<style>
.mainWindow {
    margin: 1em;
    margin-top: 2em;
    display: block;
    
}
</style>