<template>
  <main class="bg-dark">
      <div class="container">
          <div class="row d-flex justify-content-center bg-dark">
              <DiscCard v-for="disc in arrDiscs" :key="disc.poster" :disc-data ="disc" />
          </div>
      </div>
  </main>
</template>

<script>
import DiscCard from './DiscCard.vue'
import axios from 'axios'
export default {
  name: 'MainContent',
  data () {
    return {
      arrDiscs: null
    }
  },
  components: {
    DiscCard
  },
  created () {
    axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((response) => { this.arrDiscs = response.data.response })
  }

}
</script>

<style lang="scss" scoped>

</style>
