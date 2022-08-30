<template>
  <div id="app">
    <MyHeader :generiOttenutiDaCards="generiOttenutiDaCards"/>
    <MyCards @eccoIGeneri="prendoIGeneri"/>
  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue';
import MyCards from './components/MyCards.vue';


export default {
  name: 'App',
  components: {
    MyHeader,
    MyCards
  },
  data() {
    return {
      generiOttenutiDaCards: []
    }
  },
  methods: {
    prendoIGeneri(generiDaMyCards) {
      this.generiOttenutiDaCards = generiDaMyCards;
      console.log('generiOttenutiDaCards = ' + this.generiOttenutiDaCards)
    }
  }
}
</script>

<style lang="scss">
  @import './components/common.scss';
</style>
