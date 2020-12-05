<template>
  <div id="app">
  
  <div id="team" class="row row-cols-1 row-cols-lg-6  row-cols-sm-2 container-fluid mx-auto py-4 mx-2">
    <div class="col-lg-3 col-md-6 mb-4 mb-lg-0 "  v-for="(item, index) of team" :key="index">
      <TeamCard v-bind:member="item"></TeamCard>
    </div>
  </div>
  <footer-page> </footer-page>
  </div>

</template>

<script>
import FooterPage from './components/FooterPage.vue'

import TeamCard from './components/TeamCard.vue'

export default {
  name: 'App',
  components:{
    TeamCard,
    FooterPage
  },
  data(){
    return{
       team:[ {
            codigo: 1,
            nombre: 'Luis Cortés',
            descripcion: 'Universidad Libre, Ingeniería Industrial',
            rol: 'Desarrollador Front End Y Back End',
            image: './img/Luis.jpg'
            },
            {
            codigo: 2,
            nombre: 'Edson Suarez',
            descripcion: 'Universidad Industrial de Santander',
            rol: 'Desarrollador Front End',
            image: './img/Edson.jpg'
            },
            {
            codigo: 3,
            nombre: 'Omar Arias',
            descripcion: 'Ingeniería mecánica en la Universidad Distrital',
            rol: 'Desarrollador Front End',
            image: './img/omar.png'
            },
            {
            codigo: 4,
            nombre: 'Adriana Pérez',
            descripcion: 'Universidad Pedagógica y Tecnológica de Colombia.',
            rol: 'Desarrollador Front End y Back End',
            image: './img/Adriana.jpg'
            }       

  ]
    }
  }
}
</script>

