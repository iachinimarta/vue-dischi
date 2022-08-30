<template>
  <div id="app">
    <MyHeader :generiOttenutiDaCards="generiOttenutiDaCards" @valoriCambiati="prendoIlValore"/>
    <MyCards @eccoIGeneri="prendoIGeneri" :valueOttenuto="valueOttenuto"/>
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
      generiOttenutiDaCards: [],
      valueOttenuto: ''
    }
  },
  methods: {
    prendoIGeneri(generiDaMyCards) {
      this.generiOttenutiDaCards = generiDaMyCards;
    },
    prendoIlValore(newValue) {
      this.valueOttenuto = newValue;
    }
  }
}
</script>

<style lang="scss">
  @import './components/common.scss';
</style>
