<script>
export default {
  name: 'TodoComponent',
  props: ['listaTareas'] // listaTareas: Array
}
</script>
<template>
  <form @submit.prevent="agregarTarea">
    <input type="text" v-model="nuevaTarea" />
    <button type="submit">Agregar Tarea</button>
  </form>

  <ul>
    <li v-for="(tarea, idx) in listaTareas" :key="idx">
      {{ tarea }}, indice: {{ idx }}
      <button @click="$emit('eliminarTarea', idx)">Eliminar Tarea</button>
    </li>
  </ul>
</template>
<style></style>
