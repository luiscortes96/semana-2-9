<template>
  <div id="app">
    <h1 class="h1 text-center">{{titulo}}</h1>
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
      titulo : 'Noticias Colombia'
    }
  }
}
</script>

