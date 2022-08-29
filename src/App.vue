<template>
  <div id="app">
    <MyHeader/>
    <MyCards/>
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
  }
}
</script>

<style lang="scss">
  @import './components/common.scss';
</style>
