<template>
  <section id="moviesSection" class="cont__title">
    <div class="movies__inner container">
      <div class="movies__text">
        <h3>영화</h3>
        <p>더 다양한 이미지는</p>
        <a href="#">자세히</a>
      </div>
      <div class="movies__item">
        <div class="movies__img">
          <img src="@/assets/images/movie/movie01.jpg" alt="" />
        </div>
        <div class="movies__img">
          <img src="@/assets/images/movie//movie02.jpg" alt="" />
        </div>
        <div class="movies__img">
          <img src="@/assets/images/movie/movie01.jpg" alt="" />
        </div>
        <div class="movies__img">
          <img src="@/assets/images/movie/movie02.jpg" alt="" />
        </div>
        <div class="movies__img">
          <img src="@/assets/images/movie/movie01.jpg" alt="" />
        </div>
        <div class="movies__img">
          <img src="@/assets/images/movie/movie01.jpg" alt="" />
        </div>
        <div class="movies__img">
          <img src="@/assets/images/movie//movie01.jpg" alt="" />
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  props: {
    attr: String,
  },
};
</script>
<style lang="scss">
//movies__wrap
.movies__wrap {
  overflow: hidden;
}

.movies__inner {
  height: 700px;

  .movies__text {
    h3 {
      font-size: 50px;
    }

    p {
      font-size: 22px;
      font-weight: 300;
      margin: 10px 0;
    }

    a {
      width: 100px;
      height: 30px;
      background-color: var(--button_red);
      display: inline-block;
      font-weight: 300;
      color: #fff;
      line-height: 30px;
      text-align: center;
    }
  }

  .movies__item {
    position: absolute;
    margin-top: 100px;
    display: flex;

    > div {
      width: 400px;
      margin-right: 20px;
    }

    .movies__img {
      width: 270px;
      height: 400px;
      border: 1px solid var(--color_body);
      margin-left: 10px;
      overflow: hidden;

      img {
        width: 100%;
      }
    }
  }
}

//movie__slider
.movie__slider {
}

.movie__tag {
  ul {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    width: 70%;
    margin: 20px auto;
    text-align: center;

    li {
      display: inline-block;
      border: solid 1px #ffae52;
      padding: 10px 30px;
      margin: 5px;

      a {
        color: #ffae52;
      }
    }
  }
}

// unsplash page
.movie__cont {
  .movies__item {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;

    > .movies__img {
      width: 24%;
      height: 500px;
      position: relative;

      img {
      }

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

// search

.movie__search {
  text-align: center;
  margin: 50px auto;

  input {
    border: 1px solid #e8ecf2;
    font-size: 16px;
    padding: 10px 20px;
    border-radius: 50px;
    min-width: 300px;
    margin-right: 10px;
  }

  button {
    @include button(#ffae52, #fff);
    border-radius: 50px;
  }
}
</style>
