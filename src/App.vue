<template>
    <Intro />
    <NoteContainer />
</template>

<script>
import Intro from './components/Intro.vue'
import NoteContainer from './components/NoteContainer.vue'

export default {
  name: 'App',
  components: {
    Intro,
    NoteContainer

  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Josefin+Sans&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Cinzel:wght@700&display=swap');

:root {
    --font1: #ffffff;
    --font2: #C0C0C0;
    --background: #202020;
    --window: #101010;
    --innerWindow: #181818;
    --forms: #101010;
    --red: #FE0000;
    --cyan: #00FFFF;
    --dmColor: lightgreen;
    --playerColor: #D4AF37;
    --spectatorColor: grey;
    --grey: grey;
    --accentColor: #008dff;
}
body {
    background: var(--background);
    color: var(--font1);
    font-size: 16px;
    margin: 0em;
    font-family: 'Josefin Sans', sans-serif;
}
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    margin: 0px;
    padding: 0px;
}

</style>
