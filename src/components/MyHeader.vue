<template>
    <header>
        <img src="../assets/logo.svg" alt="Spotify">
        <MySelect/>
        
    </header> 
</template>

<script>
    import MySelect from './MySelect.vue';


    export default {
        name: 'MyHeader',
        components: {
            MySelect
        },
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

        img {
            width: 150px;
            margin-left: 10px;
        }
    }
</style>