<template>
  <main>
      <div class="container">
          <div class="loading" v-if="arrDiscs == null">sto caricando</div>
          <div v-else class="row d-flex justify-content-center">
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
    setInterval(() => axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((response) => { this.arrDiscs = response.data.response }), 2000
    )
    /* axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((response) => { this.arrDiscs = response.data.response }) */
  }

}
</script>

<style lang="scss" scoped>
main {
  background-color: rgb(13%, 18%, 23%);
}
.loading {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-grow: 1;
  color: white;
  text-transform: uppercase;
  font-weight: 100px;
  height: 100vh;
}

</style>
