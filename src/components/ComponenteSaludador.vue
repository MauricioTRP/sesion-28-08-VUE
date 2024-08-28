<script>
export default {
  name: 'ComponenteSaludador',
  methods: {
    saludar() {
      alert('Aloha!')
    }
  }
}
</script>
<template>
  <p @dblclick="saludar">Soy un elemento que envía alerts</p>
</template>

<style scoped></style>
