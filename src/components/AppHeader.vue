<template>
    <header id="header">
        <img src="../assets/img/logo-small.svg" alt="Logo Spotify">
    </header>
</template>

<script>
export default {
    name: "AppHeader",
}
</script>

<style lang="scss" scoped>
#header {
    padding: 1rem;
    background-color: #2e3a46;

    img {
        width: 3rem;
    }
}
</style>