<template>
    <div class="navBox">
        <p class="title">Sheet Notes<a href="/"></a></p>
        <div class="navWindow">
            <p><a href="#">Help</a></p>
            <p><a href="#">Other Projects</a></p>
            
      </div>
    </div>
</template>

<script>
    export default {
        name: 'Intro'
    }
    
</script>

<style>
a {
    text-decoration: none;
    color: inherit;
    font-family: inherit;
}

/* Title & Nav Window Styles */
.navBox {
    grid-column-start: 1;
    grid-column-end: 4;
    display: grid;
    grid-template-columns: 1fr 1fr;
    box-shadow: 4px 4px 4px 0 rgba(0, 0, 0, 0.4);
    background-color: var(--innerWindow);
    font-family: 'Josefin Sans', sans-serif;
}
.title {
    text-align: left;
    padding-left: 1em;
    margin-bottom: 0em;
    color: var(--accentColor);
}
@media screen and (max-width: 900px) {
    .navBox {
        grid-template-columns: 1fr;
    }
    .title {
        padding: 0em;
        text-align: center;
        font-size: 1.5em;
        margin-top: 0.5em;
    }
}

/* Nav Window Styles */
.navWindow {
    display: grid;
    grid-auto-flow: column;
}
.navWindow p {
    text-align: center;
    cursor: pointer;
    -webkit-touch-callout: none; /* iOS Safari */
      -webkit-user-select: none; /* Safari */
       -khtml-user-select: none; /* Konqueror HTML */
         -moz-user-select: none; /* Old versions of Firefox */
          -ms-user-select: none; /* Internet Explorer/Edge */
              user-select: none; /* Non-prefixed version, currently
                                    supported by Chrome, Edge, Opera and Firefox */
}
@media screen and (max-width: 600px) {
    .navWindow {
        grid-column-start: 1;
        grid-column-end: 2;
    }
}
</style>

