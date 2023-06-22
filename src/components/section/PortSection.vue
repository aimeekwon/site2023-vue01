<template>
  <section id="portSection" :class="attr">
    <h3>포트폴리오</h3>
    <p>포트폴리오 입니다</p>
    <div class="port__inner container">
      <div class="port__btn">more</div>
      <div class="port__cont">
        <!-- <div class="port">
          <figure class="port__header">
            <img src="@/assets/images/unsplash/unsplash01.jpg" alt="#" />
          </figure>
          <div class="port__body">
            <span>
              <img src="" alt="" />
            </span>
            <div>
              <h4>AIMEE'PORTFOLIO</h4>
              <p>프론트앤드개발자</p>
            </div>
          </div>
        </div>
        <div class="port">
          <figure class="port__header">
            <img src="@/assets/images/unsplash/unsplash01.jpg" alt="#" />
          </figure>
          <div class="port__body">
            <span>
              <img src="" alt="" />
            </span>
            <div>
              <h4>AIMEE'PORTFOLIO</h4>
              <p>프론트앤드개발자</p>
            </div>
          </div>
        </div>
        <div class="port">
          <figure class="port__header">
            <img src="@/assets/images/unsplash/unsplash01.jpg" alt="#" />
          </figure>
          <div class="port__body">
            <span>
              <img src="" alt="" />
            </span>
            <div>
              <h4>AIMEE'PORTFOLIO</h4>
              <p>프론트앤드개발자</p>
            </div>
          </div>
        </div>
        <div class="port">
          <figure class="port__header">
            <img src="@/assets/images/unsplash/unsplash01.jpg" alt="#" />
          </figure>
          <div class="port__body">
            <span>
              <img src="" alt="" />
            </span>
            <div>
              <h4>AIMEE'PORTFOLIO</h4>
              <p>프론트앤드개발자</p>
            </div>
          </div>
        </div>
        <div class="port">
          <figure class="port__header">
            <img src="@/assets/images/unsplash/unsplash01.jpg" alt="#" />
          </figure>
          <div class="port__body">
            <span>
              <img src="" alt="" />
            </span>
            <div>
              <h4>AIMEE'PORTFOLIO</h4>
              <p>프론트앤드개발자</p>
            </div>
          </div>
        </div> -->
        <div class="port" v-for="(text, index) in texts" :key="index">
          <figure class="port__header">
            <img src="text.img" alt="text.title" />
          </figure>
          <div class="port__body">
            <span> <img :src="text.icon" alt="text.title" /> </span>
            <div>
              <h4>{{ text.title }}</h4>
              <p>{{ text.dexc }}</p>
            </div>
          </div>
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
  data: function () {
    return {
      texts: [
        {
          img: "./assets/images/unsplash/unsplash01.jpg",
          title: "AIMEE'PORTFOLIO",
          desc: "프론트앤드개발자",
          icon: "",
        },
        {
          img: "./images/unsplash/unsplash01.jpg",
          title: "AIMEE'PORTFOLIO",
          desc: "프론트앤드개발자",
          icon: "",
        },
        {
          img: "./images/unsplash/unsplash01.jpg",
          title: "AIMEE'PORTFOLIO",
          desc: "프론트앤드개발자",
          icon: "",
        },
        {
          img: "./images/unsplash/unsplash01.jpg",
          title: "AIMEE'PORTFOLIO",
          desc: "프론트앤드개발자",
          icon: "",
        },
        {
          img: "./images/unsplash/unsplash01.jpg",
          title: "AIMEE'PORTFOLIO",
          desc: "프론트앤드개발자",
          icon: "",
        },
        {
          img: "./images/unsplash/unsplash01.jpg",
          title: "AIMEE'PORTFOLIO",
          desc: "프론트앤드개발자",
          icon: "",
        },
      ],
    };
  },
};
</script>
<style lang="scss">
//portfolio
.port__wrap {
  text-align: center;
  h3 {
    font-size: 50px;
  }
  p {
    font-size: 22px;
    font-weight: 300;
    margin: 10px 0;
  }
}
.port__inner {
  .port__btn {
    width: 100px;
    height: 30px;
    background-color: var(--button_red);
    display: inline-block;
    font-weight: 300;
    color: #fff;
    line-height: 30px;
    text-align: center;
  }
  .port__cont {
    @include flex-between;
    flex-wrap: wrap;
    .port {
      width: 31%;
      display: inline-block;
      margin-top: 20px;
      .port__header {
        border-radius: 10px;
        border: 1px solid var(--color_body);
        width: 100%;
        height: 200px;
        overflow: hidden;
        img {
          width: 100%;
        }
      }

      .port__body {
        width: 100%;
        display: flex;
        margin-top: 10px;
        span {
          width: 30px;
          height: 30px;
          border: 1px solid var(--color_body);
          display: inline-block;
          margin-right: 10px;
          line-height: 30px;
        }
        > div {
          h4 {
            font-weight: 900px;
            font-size: 18px;
          }
        }
      }
    }
  }
}
</style>
