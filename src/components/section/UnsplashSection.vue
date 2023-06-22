<template>
  <section id="unsplashSection" :class="attr">
    <div class="unsplash__inner container">
      <div class="unsplash__text">
        <h3>언스플래쉬</h3>
        <p>더 다양한 이미지는</p>
        <a href="#">자세히</a>
      </div>

      <div class="unsplash__item">
        <div class="unsplash__img">
          <img src="@/assets/images/unsplash/unsplash01.jpg" alt="" />
        </div>
        <div class="unsplash__img">
          <img src="@/assets/images/unsplash/unsplash02.jpg" alt="" />
        </div>
        <div class="unsplash__img">
          <img src="@/assets/images/unsplash/unsplash01.jpg" alt="" />
        </div>
        <div class="unsplash__img">
          <img src="@/assets/images/unsplash/unsplash02.jpg" alt="" />
        </div>
        <div class="unsplash__img">
          <img src="@/assets/images/unsplash/unsplash01.jpg" alt="" />
        </div>
        <div class="unsplash__img">
          <img src="@/assets/images/unsplash/unsplash02.jpg" alt="" />
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
//unsplash
.unsplash__wrap {
  overflow: hidden;
}

.unsplash__inner {
  height: 500px;
  .unsplash__text {
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

  .unsplash__item {
    position: absolute;
    margin-top: 100px;
    display: flex;
    > div {
      width: 400px;
      margin-right: 20px;
    }
    .unsplash__img {
      width: 350px;
      height: 200px;
      border: 1px solid var(--color_body);
      margin-left: 10px;
      overflow: hidden;
      img {
        width: 100%;
      }
    }
  }
}

// unsplash page
.unsplash__cont {
  ul {
    column-count: 4;
    li {
      margin: 20px;
    }
  }
}
// search

.unsplash__search {
  text-align: center;
  margin-bottom: 50px;
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
