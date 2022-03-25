<template>
  <select class="form-select col-4" aria-label="Default select example" @change="onChange"> <!--  -->
    <option value="" selected>Filtra per Genere</option>
    <option v-for="genre in arrDiscs" :key="genre" :value="genre">{{genre}}</option>
  </select>
</template>

<script>
export default {
  name: 'SearchGenereA',
  data () {
    return {
      genere: ''
    }
  },
  methods: {
    onChange (event) {
      this.genere = event.target.value
      console.log(this.genere)
      this.$emit('search', this.genere)
    }
  }
}
</script>

<style>

</style>
