<script>
// import ComponenteSaludador from './components/ComponenteSaludador.vue'
// import TodoComponent from './components/TodoComponent.vue'
// import KeyEvents from './components/KeyEvents.vue'
import HeaderComponent from './components/HeaderComponent.vue'
import HeroComponent from './components/HeroComponent.vue'
import PersonCard from './components/PersonCard.vue'
import InstrumentsCard from './components/InstrumentsCard.vue'

export default {
  components: {
    HeaderComponent,
    HeroComponent,
    PersonCard,
    InstrumentsCard
  },
  data() {
    return {
      personas: [
        {
          nombre: 'Evan You',
          foto: 'https://miro.medium.com/v2/resize:fit:500/0*xkJgg-6HskYrQ3N7.jpeg',
          descripcion: 'Creador de VueJS'
        },
        {
          nombre: 'Evan Me',
          foto: 'https://miro.medium.com/v2/resize:fit:500/0*xkJgg-6HskYrQ3N7.jpeg',
          descripcion: 'Creador de JSON'
        },
        {
          nombre: 'Evan They',
          foto: 'https://miro.medium.com/v2/resize:fit:500/0*xkJgg-6HskYrQ3N7.jpeg',
          descripcion: 'Creador de CURL'
        }
      ],
      instrumentos: [
        {
          nombre: 'Batería Electrónica',
          foto: 'https://cdn.webshopapp.com/shops/321836/files/444339901/image.jpg',
          precio: '649.900'
        },
        {
          nombre: 'Guitarra Eléctrica',
          foto: 'https://glitterguitars.com/images/8/Crystallized-RG-Prestige-electric-guitar-4.jpg',
          precio: '429.900'
        },
        {
          nombre: 'Teclado',
          foto: 'https://m.media-amazon.com/images/I/51TivJrmiaL._AC_.jpg',
          precio: '499.900'
        }
      ]
    }
  }
}
</script>

<template>
  <HeaderComponent />
  <!-- <HeroComponent />
  <div class="personas">
    <PersonCard
      v-for="(persona, idx) in personas"
      :key="idx"
      :nombre="persona.nombre"
      :foto="persona.foto"
      :descripcion="persona.descripcion"
    />
  </div> -->

  <div class="instrumento">
    <InstrumentsCard
      v-for="(instrumento, index) in instrumentos"
      :key="index"
      :nombre="instrumento.nombre"
      :foto="instrumento.foto"
      :precio="instrumento.precio"
    />
  </div>
</template>

<style scoped>
.personas {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}
.instrumento {
  margin: 2rem;
  display: flex;
  column-gap: 2rem;
  justify-content: center;
}
</style>
