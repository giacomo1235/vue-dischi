<template>
  <div id="app">
    <HeaderDischi @search="searchRilevato"/>
    <MainContent :search-string="this.genere"/>
    <FooterDischi />
  </div>
</template>

<script>
import HeaderDischi from './components/HeaderDischi.vue'
import MainContent from './components/MainContent.vue'
import FooterDischi from './components/FooterDischi.vue'

export default {
  name: 'App',
  components: {
    HeaderDischi,
    MainContent,
    FooterDischi
  },
  data () {
    return {
      genere: ''
    }
  },
  methods: {
    searchRilevato (datiComponente) {
      this.genere = datiComponente
      console.log(datiComponente)
    }
  }
}
</script>

<style lang="scss">
@import "~bootstrap/scss/bootstrap";
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
