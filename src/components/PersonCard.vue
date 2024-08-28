<script>
export default {
  name: 'PersonCard',
  props: ['nombre', 'foto', 'descripcion']
}
</script>
<template>
  <div class="persona">
    <div class="avatar" :style="{ backgroundImage: `url(${foto})` }"></div>
    <h2>{{ nombre }}</h2>
    <p>{{ descripcion }}</p>
  </div>
</template>
<style>
.avatar {
  background-size: cover;
  background-position: center;
  height: 200px;
  width: 200px;
  border-radius: 50%;
}

.persona {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
