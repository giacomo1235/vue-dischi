<template>
  <div id="app">
    <HeaderDischi/>
    <MainContent />
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

  }
}
</script>

<style lang="scss">
@import "../node_modules/bootstrap/scss/bootstrap";
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
