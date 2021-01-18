<template lang="html" id="film">
    <div v-if='film'>
         <div id ="film">
        
        <h3>{{film.title}}</h3>
        <p>Director: {{film.director}}</p>
        <p>Year: {{film.release_date}}</p>
        <p>Description: {{film.description}}</p>
        <p>Rating: {{film.rt_score}}</p>
     </div>
    </div>
</template>

<script>
export default {
    name: "film-detail", 
    props: ['film']
}
</script>
<<style scoped>

#film {
  position: absolute;
    top: 13%;
    left: 50%;
    margin-top: -50px;
    margin-left: -50px;
    width: 200px;
    height: 100px;
    background-color: blue;
    }
#beer-info {
  display: flex;
  
}
p {
  font: 13px Futura;
    display: flex;
    
    

  
}
li {
  font: 10px Futura;
}
#picture {
  display: flex;
  flex-direction: column;
  width: 200px;
  padding: 20px;
}
#ingredientsContainer {
  display: flex;
  justify-content: space-evenly;
  padding-bottom: 60px;
}
#film-text {
  margin-left: 1000%;
  margin-right: 10%;
  word-wrap: normal;
}
img {
  height: 325px;
  width: 150px;
}
h3 {
  font: bold 15px Futura;
}
.ingredient {
  padding-left: 15px;
  padding-right: 30px;
  border-radius: 25px;
  border: 2px solid dodgerblue;
  background-color: white;
}
</style>
