<template>
    <div>
        <audio autoplay id="audio-player" loop>
            <source src=".././assets/musics/intro1.ogg" type="audio/ogg" />
        </audio>
    </div>
</template>

<script>
export default {
    name: 'IntroVue',
}
</script>

<style>
#audio-player {
    display: none;
}
</style>