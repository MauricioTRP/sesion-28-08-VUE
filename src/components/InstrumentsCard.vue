<script>
export default {
  name: 'InstrumentsCard',
  props: ['foto', 'nombre', 'precio']
}
</script>
<template>
  <div class="card" :style="{ backgroundImage: `url(${foto})` }">
    <h1>{{ nombre }}</h1>
    <p>${{ precio }}</p>
  </div>
</template>
<style scoped>
.card {
  width: 20%;
  text-align: center;
  background-position: top center;
  background-size: 100px;
  background-repeat: no-repeat;
  border: 1px solid lightgray;
  padding: 1rem;
}
h1 {
  margin-top: 5.5rem;
  font-size: 1.2rem;
}
</style>
