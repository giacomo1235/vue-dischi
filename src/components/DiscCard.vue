<template>
  <div class="col-6 col-md-3 col-lg-2 card-disc">
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
  background-color: rgb(19%, 23%, 27%);
    margin: 1rem;
    padding: 1rem;
}

h2  {
  font-size: 1.5rem;
  text-transform: uppercase;
  color: white;
  font-weight: 600;
    &::after {
        content: '';
        display: block;
        margin: .5rem auto;
        padding: .5rem;
        width: 50%;
    }
}
h3,
h4 {
  color: rgb(39%, 39%, 39%);
}
</style>
