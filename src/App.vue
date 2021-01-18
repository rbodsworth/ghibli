<template>
  <div>
    <div class="main-container">
      <h1>Films</h1>
      <films-list :films='films'></films-list>
      <film-detail :film='selectedFilm'></film-detail>
    
    </div>
  </div>
</template>

<script>
  import { eventBus } from './main.js'
  import FilmsList from './components/FilmsList.vue';
  import FilmsDetail from './components/FilmsDetail.vue';


export default {
   name: 'app',
   data(){
     return {
       films: [],
       selectedFilm: null
     };
   
  },
   mounted(){
     fetch("https://ghibliapi.herokuapp.com/films")
     .then( res => res.json())
     .then(films => this.films = films)
     eventBus.$on('film-selected', (film) => {
       this.selectedFilm = film;
   })
     },
    components: {
      "films-list": FilmsList,
      "film-detail": FilmsDetail, 
   

    }
}
</script>

<style>
  
  .main-container {
    display: flex;
    justify-content: space-between;
  }
</style>