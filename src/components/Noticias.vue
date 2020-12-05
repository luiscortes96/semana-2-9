<template>
    <div class="row container-fluid mx-auto">
        <div v-for="item in informacion" v-bind:key="item.id" class="col-xl-3 col-lg-4 col-md-6 col-sm-6 mx-auto my-3">
            <div class="card  mb-3 h-100">
                <img class="card-img-top"  v-bind:src="item.urlToImage" v-bind:alt="item.title">
                <div class="card-body">
                    <h5 class="card-title">{{item.title}}</h5>
                    <p class="card-text text-justify">{{item.description}}</p>
                    <a v-bind:href="item.url" class="btn btn-primary">Ver más</a>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import axios from 'axios'
export default {
    name: 'Noticias',
    props: {

    }, 
    data(){
        return{
            informacion:[] ,
            titulo : 'Noticias de la semana'

        }
  },
  
  mounted (){
      axios
      .get('http://newsapi.org/v2/top-headlines?country=co&apiKey=d7f504a8743c44e19015be237c251dcc')
      .then(respuesta =>this.informacion=respuesta.data.articles)
      
  }  
}



</script>

<style scoped>

</style>