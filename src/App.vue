<template>
  <div id="app">
    <img  id="reel" alt="Reel" src="./assets/reel.jpg">
    <header>Search for a movie:</header>
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

<style scoped>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

#reel {
  height: 15em;
}
</style>