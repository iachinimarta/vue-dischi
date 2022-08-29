<template>
  <div class="card-container">
        <div class="wrapper">
            <img :src="cardsList.poster" :alt="cardsList.name">
            <h5 class="title">{{cardsList.title.toUpperCase()}}</h5>
            <h6>{{cardsList.author}}</h6>
            <h6>{{cardsList.year}}</h6>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'MySingleCard',
        props: {
            cardsList: Object
        }
    }
</script>

<style lang="scss">
   .card-container {
        display: inline-block;
        width: calc(100% / 5 - 20px);
        background-color: #2E3A46;
        margin: 10px;

        .wrapper {
            padding: 10px;
            text-align: center;

            img {
                width: 100%;
                height: 120px;
            }

            .title {
                color: white;
                margin-bottom: 10px;
            }

            h6 {
                color: grey;
            }
        }
    }

</style>