<template>
    <div class="row px-5">
        <div v-for="item in informacion" :key="item.id" class=".col-6 .col-md-4 mx-auto my-4"> 
           <div class="card mb-3 h-100" style="max-width: 550px;">
                <div class="row no-gutters">
                    <div class="col-md-4">
                         <!-- <img src="{{ item.urlToImage }}" class="card-img" alt="..."> -->
                    </div>
                    <div class="col-md-8">
                         <div class="card-body">
                            <h5 class="card-title">{{ item.title }}</h5>
                            <p class="card-text">{{ item.description }}</p>
                            <p class="card-text"><small class="text-muted">{{ item.publishedAt }}</small></p>
                        </div>
                    </div>
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