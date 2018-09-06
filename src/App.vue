<template>
  <div id="app">
    <img  id="reel" alt="Reel" src="./assets/reel.jpg">
    <header class="intro">Search for a movie:</header>
    <input type="text" placeholder="Movie Search"/>
    <MovieList />
  </div>
</template>

<script>
import MovieList from "./components/MovieList.vue";

export default {
  name: "app",
  components: {
    MovieList
  }
};
</script>

<style>

@import url('https://fonts.googleapis.com/css?family=ABeeZee|Caveat|Poiret+One');
/* font-family: 'ABeeZee', sans-serif;
font-family: 'Poiret One', cursive;
font-family: 'Caveat', cursive; */
#app {
  font-family: 'Caveat', cursive;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  /* margin-top: 60px; */
  /* background: #EAF2EF; */
  margin-right: 3em;
}

#reel {
  height: 15em;
}

.intro {
  font-family: 'Poiret One', cursive;
  font-size: 22px;
}
</style>