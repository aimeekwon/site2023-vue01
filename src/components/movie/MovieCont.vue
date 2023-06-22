<template>
  <div class="movie__cont container">
    <div class="movies__item">
      <ul>
        <li v-for="(movie, index) in movies" :key="index">
          <a
            :href="`https://www.themoviedb.org/movie/${movie.id}`"
            target="_blank"
          >
            <img
              :src="`https://image.tmdb.org/t/p/w500${movie.poster_path}`"
              :alt="movie.title"
            />
          </a>
          <em>
            <span class="title">{{ movie.title }}</span>
            <span class="star">{{ movie.vote_average }}</span>
          </em>
        </li>
      </ul>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    movies: {
      type: Array,
      required: true,
    },
  },
};
</script>
<style lang="scss">
.movie__cont {
  .movies__item {
    ul {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;

      > li {
        width: 24%;
        height: 500px;
        position: relative;

        .title {
          margin-bottom: 2%;
          display: inline-block;
          padding: 3px 0;
          font-size: 20px;

          &:hover {
            text-decoration: underline;
            text-underline-position: under;
          }
        }

        .star {
          position: absolute;
          right: 20px;
          top: 20px;
          width: 30px;
          height: 30px;
          background-color: #fff;
          text-align: center;
          border-radius: 50%;
          font-size: 12px;
          line-height: 30px;
          font-weight: bold;
          color: #7c7c7c;
        }
      }
    }
  }
}
</style>
