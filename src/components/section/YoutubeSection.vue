<template>
  <section id="youtubeSection" :class="attr">
    <div class="youtube__inner container">
      <div class="youtube__text">
        <h3>유튜브</h3>
        <p>더 다양한 강의는 유튜브에서</p>
        <a href="#">자세히</a>
      </div>
      <div class="youtube__item">
        <div class="you__play">
          <img src="@/assets/images/youtube/you01.jpg" alt="" />
        </div>
        <div class="you__play">
          <img src="@/assets/images/youtube/you02.jpg" alt="" />
        </div>
        <div class="you__play">
          <img src="@/assets/images/youtube/you01.jpg" alt="" />
        </div>
        <div class="you__play">
          <img src="@/assets/images/youtube/you02.jpg" alt="" />
        </div>
        <div class="you__play">
          <img src="@/assets/images/youtube/you01.jpg" alt="" />
        </div>
        <div class="you__play">
          <img src="@/assets/images/youtube/you02.jpg" alt="" />
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
//youtube__wrap
.youtube__wrap {
  overflow: hidden;
}

.youtube__inner {
  height: 500px;

  .youtube__text {
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

  .youtube__item {
    position: absolute;
    margin-top: 100px;
    display: flex;

    > div {
      width: 400px;
      margin-right: 20px;
    }

    .you__play {
      width: 350px;
      height: 180px;
      border: 1px solid var(--color_body);
      margin-left: 10px;
      overflow: hidden;

      img {
        width: 100%;
      }
    }
  }
}

//youtube page
//.youtube__page {}

.youtube__slider {
  display: none;
}

.youtube__search {
  text-align: center;
  margin: 50px;

  input {
    border: 1px solid #e8ecf2;
    font-size: 16px;
    padding: 10px 20px;
  }

  button {
    @include button(#475ee4, #fff);
  }
}

.youtube__tag {
  text-align: center;
  ul {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    margin-bottom: 50px;
    margin-top: 100px;

    li {
      a {
        border: 1px solid gray;
        padding: 10px 20px;
        margin: 0 10px;
        color: red;
        border: 1px solid red;
      }
    }
  }
}

.youtube__cont {
  text-align: center;

  ul {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    margin-bottom: 100px;

    li {
      width: 24%;
      margin-bottom: 4%;
      overflow: hidden;
      white-space: nowrap;
      text-overflow: ellipsis;
      -webkit-line-clamp: 1; /* 라인수 */
      -webkit-box-orient: vertical;
      word-wrap: break-word;
    }
  }
}
</style>
