<template>
  <div id="app">
  
  <div class="row row-cols-4 row-cols-lg-4 container-fluid mx-auto py-4  ">
  <div class="col-lg-3 col-md-6 mb-4 mb-lg-0" v-for="(item, index) of team" :key="index">
  <TeamCard v-bind:member="item"></TeamCard>
  
  </div>
  </div>
  </div>

</template>

<script>

import TeamCard from './components/TeamCard.vue'

export default {
  name: 'App',
  components:{
    TeamCard
  },
  data(){
    return{
      title:'Hola',
       team:[ {
            codigo: 1,
            nombre: 'Luis Cortés',
            descripcion: 'Universidad Libre, Ingeniería Industrial Pasatiempo: Leer, tocar un instrumento musical guitarra luiscortes1996@hotmail.com',
            rol: 'Desarrollador Front End Y Front End',
            image: './img/Luis.jpg'
            },
            {
            codigo: 2,
            nombre: 'Edson Suarez',
            descripcion: 'Universidad Industrial de Santander Pasatiempo: Jugar videojuegos, tocar guitarra, practicar baloncesto, filososfar edsondz43@gmail.com',
            rol: 'Desarrollador Front End',
            image: './img/Edson.jpg'
            },
            {
            codigo: 3,
            nombre: 'Omar Arias',
            descripcion: 'Ingeniería mecánica en la Universidad Distrital. Pasatiempo:leer, dibujar, escuchar música y practicar inglés y alemán omar_9478@hotmail.com',
            rol: 'Desarrollador Front End Y Front End',
            image: './img/omar.png'
            },
            {
            codigo: 4,
            nombre: 'Adriana Pérez',
            descripcion: 'Universidad Pedagógica y Tecnológica de Colombia Pasatiempo: Leer, Ver Series adrianaperez.crist@gmail.com',
            rol: 'Desarrollador Front End',
            image: './img/Adriana.jpg'
            }       

  ]
    }
  }
}
</script>

