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



export default {
  name: 'App',
  components: {
    Noticias,
    FooterPage
  },

  data(){
    return{
      titulo :'Noticias del País'
    }
  }
}
</script>

