<template>
  <div>
    <main>
      <ContTitle title="movies" />
      <MovieSearch />
      <MovieSlider />
      <MovieTag />
      <MovieCont :movies="movies" />
    </main>
  </div>
</template>

<script>
import ContTitle from "@/components/layout/ContTitle.vue";
import MovieSearch from "@/components/movie/MovieSearch.vue";
import MovieSlider from "@/components/movie/MovieSlider.vue";
import MovieTag from "@/components/movie/MovieTag.vue";
import MovieCont from "@/components/movie/MovieCont.vue";
import { ref } from "vue";

export default {
  components: {
    ContTitle,
    MovieSearch,
    MovieSlider,
    MovieTag,
    MovieCont,
  },

  setup() {
    const movies = ref([]);

    const TopMovies = async () => {
      await fetch(
        "https://api.themoviedb.org/3/movie/popular?api_key=5c70be62052630089093f57524dd2c17&limit=30"
      )
        .then((response) => response.json())
        .then((result) => {
          console.log(result.results);
          movies.value = result.results;
        })
        .catch((error) => console.log("error", error));
    };
    TopMovies();

    return {
      movies,
      TopMovies,
    };
  },
};
</script>
