<template>
  <div class="col-6 col-md-3 col-lg-2 card-disc bg-light">
      <img class="img-fluid" :src="discData.poster" :alt="discData.author">
      <h2>{{discData.title}}</h2>
      <h3>{{discData.author}}</h3>
      <h4>{{discData.year}}</h4>
  </div>
</template>

<script>
export default {
  name: 'DiscCard',
  props: {
    discData: Object
  }

}
</script>

<style lang="scss" scoped>
.card-disc {
    margin: .5rem;
    padding: .5rem;
}

h2  {
    &::after {
        content: '';
        display: block;
        margin: .5rem auto;
        padding: .5rem;
        width: 50%;
    }
}
</style>
