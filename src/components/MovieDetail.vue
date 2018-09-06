<template>
<div class="flip-container" ontouchstart="this.classList.toggle('hover');">
	<div class="flipper">
		<div class="front">
			<header>{{movieResult.title}}</header>
            <img :src="addImage(movieResult.poster_path)" alt="poster"/>
		</div>
		<div class="back">
			<footer>Release Date: {{movieResult.release_date}}</footer>
            <p>{{movieResult.overview}}</p>
		</div>
	</div>
</div>

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
  height: 24em;
  width: 15em;
  border-radius: 1em;
}

ul {
  background: #eaf3ea;
}

header {
  font-size: 24px;
}

p {
    font-size: 3vh; 
    /* font-size: 2vw; */
}

/* entire container, keeps perspective */
.flip-container {
  perspective: 1000px;
  border: 1px solid black;
  margin: 5px 5px;
  padding: 5px;
  background: #eaf3ea;
}
/* flip the pane when hovered */
.flip-container:hover .flipper,
.flip-container.hover .flipper {
  transform: rotateY(180deg);
}

.flip-container,
.front,
.back {
  width: 320px;
  height: 480px;
}

/* flip speed goes here */
.flipper {
  transition: 0.6s;
  transform-style: preserve-3d;

  position: relative;
}

/* hide back of pane during swap */
.front,
.back {
  backface-visibility: hidden;
  position: absolute;
  top: 0;
  left: 0;
}

/* front pane, placed above back */
.front {
  z-index: 2;
  transform: rotateY(0deg);

}

/* back, initially hidden pane */
.back {
  transform: rotateY(180deg);
  justify-content: center;;
}
</style>