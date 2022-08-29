<template>
    <div>       
        <div class="card-wrapper d-flex">
            <MySingleCard v-for="(card, index) in cardsList" :key="index" :cardsList="card"/>         
        </div>

        <button @click="generiOttenuti">Prova</button>
        <button @click="$emit('eccoIGeneri', generiDaMyCards)">prova due</button>
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
                generiDaMyCards: [],
                cardsList: [],
                endpoint: 'https://flynn.boolean.careers/exercises/api/array/music',
            }
        },
        created() {
           axios.get(this.endpoint)
            .then(reply => {
                this.cardsList = reply.data.response;
                console.log(reply.data.response);           
            })
        },
        methods: {
            generiOttenuti() {
                this.generiDaMyCards = this.cardsList.map(obj => obj.genre);
                console.log('generiDaMyCards = ' + this.generiDaMyCards);
            }
        }
    }
</script>

<style lang="scss">
    @import 'common.scss';

    .card-wrapper {
        width: 70%;
        margin: auto;
        flex-wrap: wrap;
        padding: 50px;
    }


</style>