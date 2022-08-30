<template>
    <header>
        <img src="../assets/logo.svg" alt="Spotify">
        <select class="select-genres" name="genres" id="genres">
            <option v-for="(genere, index) in generiOttenutiDaCards" :key="index" :value="genere">{{genere}}</option>
        </select>        
    </header> 
</template>

<script>
    export default {
        name: 'MyHeader',
        props: {
            generiOttenutiDaCards: Array
        }
    }
</script>

<style scoped lang="scss">
    header {
        width: 100%;
        height: 80px;
        background-color: #2E3A46;
        display: flex;
        align-items: center;
        justify-content: space-between;

        .select-genres {
            margin-right: 10px;
        }

        img {
            width: 150px;
            margin-left: 10px;
        }
    }
</style>