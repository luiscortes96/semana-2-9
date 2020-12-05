<template>
  <div id="app">
    <h1 class="h1 text-center text-info">{{titulo}}</h1>
    <Noticias></Noticias>
  </div>
</template>

<script>
import Noticias from './components/Noticias.vue'

export default {
  name: 'App',
  components: {
    Noticias
  },
  data(){
    return{
      titulo :'Noticias del País'
    }
  }
}
</script>

