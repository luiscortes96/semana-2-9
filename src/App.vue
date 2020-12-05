<template>
  <div id="app">
    <h1 class="h1 text-center text-info">{{titulo}}</h1>
    <Noticias></Noticias>
    <div id="team" class="row row-cols-1 row-cols-lg-6  row-cols-sm-2 container-fluid mx-auto py-4 mx-2">
      <div class="col-lg-3 col-md-6 mb-4 mb-lg-0 "  v-for="(item, index) of team" :key="index">
        <TeamCard v-bind:member="item"></TeamCard>
      </div>
    </div>
    <footer-page> </footer-page>
  </div>
</template>

<script>
import Noticias from './components/Noticias.vue'
import FooterPage from './components/FooterPage.vue'
import TeamCard from './components/TeamCard.vue'


export default {
  name: 'App',
  components: {
    Noticias,
    FooterPage,
    TeamCard
  },

  data(){
    return{
      titulo :'Noticias del País',
      team:[ {
            codigo: 1,
            nombre: 'Luis Cortés',
            descripcion: 'Universidad Libre, Ingeniería Industrial Pasatiempo: Leer, tocar un instrumento musical guitarra.',
            rol: 'Desarrollador Front End Y Front End',
            image: './img/Luis.jpg'
            },
            {
            codigo: 2,
            nombre: 'Edson Suarez',
            descripcion: 'Universidad Industrial de Santander Pasatiempo: Jugar videojuegos, tocar guitarra, practicar baloncesto, filososfar.',
            rol: 'Desarrollador Front End',
            image: './img/Edson.jpg'
            },
            {
            codigo: 3,
            nombre: 'Omar Arias',
            descripcion: 'Ingeniería mecánica en la Universidad Distrital. Pasatiempo:leer, dibujar, escuchar música y practicar inglés y alemán.',
            rol: 'Desarrollador Front End Y Front End',
            image: './img/omar.jpg'
            },
            {
            codigo: 4,
            nombre: 'Adriana Pérez',
            descripcion: 'Universidad Pedagógica y Tecnológica de Colombia Pasatiempo: Leer, Ver Series.',
            rol: 'Desarrollador Front End',
            image: './img/Adriana.jpg'
            } ]
    }
  }
}
</script>

