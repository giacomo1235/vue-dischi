<template>
  <nav class="navbar">
    <div class="container">
      <div class="row justify-content-center">
        <a class="navbar-brand col-4" href="#">
          <img src="Spotify_logo_without_text.svg.png" alt="" width="30" height="24">
        </a>
        <SearchGenere @search="setSearchString" />      </div>
    </div>
  </nav>
</template>

<script>
import SearchGenere from './SearchGenere.vue'
export default {
  name: 'HeaderDischi',
  data () {
    return {
      stringRicerca: ''
    }
  },
  methods: {
    setSearchString (datiComponente) {
      this.$emit('search', datiComponente)
    }
  },
  components: {
    SearchGenere
  }
}
</script>

}
<style lang="scss" scoped>
img {
  width: 50px;
  height: 50px;
}
.navbar {
    margin-top: -60px;
    background-color: rgb(19%, 23%, 27%);
}

</style>
