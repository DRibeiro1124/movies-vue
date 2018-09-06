<template>
<ul>
    <header>{{movieResult.title}}</header>
    <img :src="addImage(movieResult.poster_path)" alt="poster"/>
    <footer>Release Date: {{movieResult.release_date}}</footer>
    <p>{{movieResult.overview}}</p>
</ul>
</template>

<script>
export default {
  name: "MovieDetail",
  props: {
    movieResult: Object
  },
  data: function() {
    return {};
  },
  methods: {
    addImage: function(poster_path) {
      return "https://image.tmdb.org/t/p/w500/" + poster_path;
    }
  }
};
</script>

<style scoped>
img {
    height: 20em;
    width: 15em;
    border-radius: 1em;
}

ul {
    background: #EAF3EA;
}

header {
    font-size: 24px;
}


</style>