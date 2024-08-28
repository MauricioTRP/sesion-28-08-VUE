<script>
export default {
  name: 'TodoComponent',
  data() {
    return {
      nuevaTarea: '',
      tareas: []
    }
  },
  methods: {
    agregarTarea() {
      // Variable temporal para obtener la nueva tarea
      const tareaAgregar = this.nuevaTarea

      // Push al arreglo de tareas
      this.tareas.push(tareaAgregar)

      // Limpiamos variable de estado nuevaTarea
      this.nuevaTarea = ''

      console.log(this.tareas)
    }
  }
}
</script>
<template>
  <form @submit.prevent="agregarTarea">
    <input type="text" v-model="nuevaTarea" />
    <button type="submit">Agregar Tarea</button>
  </form>

  <ul>
    <li v-for="(tarea, idx) in tareas" :key="idx">{{ tarea }}, indice: {{ idx }}</li>
  </ul>
</template>
<style></style>
