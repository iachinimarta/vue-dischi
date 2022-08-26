<template>
  <div>   
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
    width: 80px;
    height: 80px;

        img {
            width: 100%;
        }

        h4 {
            color: blck;
        }
   }

</style>