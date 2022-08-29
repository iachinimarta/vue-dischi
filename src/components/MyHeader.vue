<template>
    <header>
        <img src="../assets/logo.svg" alt="Spotify">
    </header> 
</template>

<script>
    export default {
        name: 'MyHeader'
    }
</script>

<style scoped lang="scss">
    header {
        width: 100%;
        height: 80px;
        background-color: #2E3A46;
        display: flex;
        align-items: center;

        img {
            width: 150px;
            margin-left: 10px;
        }
    }
</style>