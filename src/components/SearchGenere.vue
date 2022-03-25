<template>
  <select class="form-select col-4" aria-label="Default select example" @change="onChange"> <!--  -->
          <option selected>Filtra per Genere</option>
          <option value="rock">Rock</option>
          <option value="pop">Pop</option>
          <option value="jazz">Jazz</option>
          <option value="metal">Metal</option>
        </select>
</template>

<script>
export default {
  name: 'SearchGenere',
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
