<template>
    <div>
        <div>
            <MySingleCard v-for="(card, index) in cardsList" :key="index"/>         
        </div>    
    </div>
</template>

<script>
    import axios from 'axios';
    import MySingleCard from './MySingleCard.vue';

    export default {
        name: 'MyCards',
        components: {
            MySingleCard
        },
        data() {
            return {
                cardsList: '',
                endpoint: 'https://flynn.boolean.careers/exercises/api/array/music'
            }
        },
        created() {
           axios.get(this.endpoint)
            .then(reply => {
                this.cardsList = reply.data.response;
                console.log(reply.data.response)
            })
        }
    }
</script>

<style>

</style>