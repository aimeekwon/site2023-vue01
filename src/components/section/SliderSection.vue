<template>
  <section id="sliderSection" :class="attr">
    <div class="slider__inner">
      <!--<h2 class="blind">배너 슬라이더</h2>
      <div class="slider__img">
        <div class="silder s1 container">
          <div class="text">
            <h3>FOR <br />YOGA</h3>
            <p>DESIRE<br />IMAGINE/</p>
            <a href="#" class="more button-blue">more</a>
          </div>
          <div class="img" aria-label="hidden">
            <img src="@/assets/images/slider/slider_icon01.png" alt="이미지" />
            <img src="@/assets/images/slider/slider_icon03.png" alt="이미지" />
            <img src="@/assets/images/slider/slider_icon07.png" alt="이미지" />
          </div>
          <div class="circle" aria-label="hidden">
            <span class="circle c1"></span>
            <span class="circle c2"></span>
            <span class="circle c3"></span>
            <span class="circle c4"></span>
            <span class="circle c5"></span>
          </div>
        </div>

        <div class="silder s2">
          <h3>New <br>portfolio</h3>
          <p>DESIRE<br>IMAGINE/</p>
          <a href="#">more</a>
        </div>
        <div class="silder s3">
          <h3>New <br>portfolio</h3>
          <p>DESIRE<br>IMAGINE/</p>
          <a href="#">more</a>
        </div> 
      </div>
      <div class="slider__btn">
        <a href="#" class="left"><span class="ir">이전이미지</span></a>
        <a href="#" class="right"><span class="ir">다음이미지</span></a>
      </div>
      <div class="slider__dot">
        <a href="#" class="dot active"><span class="ir">1번 이미지</span></a>
        <a href="#" class="dot"><span class="ir">2번 이미지</span></a>
        <a href="#" class="dot"><span class="ir">3번 이미지</span></a>
      </div>-->

      <swiper
        :modules="modules"
        :slides-per-view="1"
        :space-between="50"
        navigation
        :pagination="{ clickable: true }"
        :autoplay="{
          delay: 2500,
          disableOnInteraction: false,
        }"
        @swiper="onSwiper"
        @slideChange="onSlideChange"
      >
        <swiper-slide v-for="(slider, index) in sliders" :key="index">
          <div class="slider__img">
            <div class="silder s1 container">
              <div class="text">
                <h3 v-html="slider.title"></h3>
                <p v-html="slider.desc"></p>
                <a href="#" class="more button-blue">more</a>
              </div>
              <div class="img" aria-label="hidden">
                <img :src="slider.iconImage1" :alt="slider.title" />
                <img :src="slider.iconImage2" :alt="slider.title" />
                <img :src="slider.iconImage3" :alt="slider.title" />
              </div>
              <div class="circle" aria-label="hidden">
                <span class="circle c1"></span>
                <span class="circle c2"></span>
                <span class="circle c3"></span>
                <span class="circle c4"></span>
                <span class="circle c5"></span>
              </div>
            </div>
          </div>
        </swiper-slide>
        <swiper-slide v-for="(slider, index) in sliders" :key="index">
          <div class="slider__img">
            <div class="silder s1 container">
              <div class="text">
                <h3 v-html="slider.title"></h3>
                <p v-html="slider.desc"></p>
                <a href="#" class="more button-blue">more</a>
              </div>
              <div class="img" aria-label="hidden">
                <img :src="slider.iconImage4" :alt="slider.title" />
                <img :src="slider.iconImage5" :alt="slider.title" />
                <img :src="slider.iconImage6" :alt="slider.title" />
              </div>
              <div class="circle" aria-label="hidden">
                <span class="circle c1"></span>
                <span class="circle c2"></span>
                <span class="circle c3"></span>
                <span class="circle c4"></span>
                <span class="circle c5"></span>
              </div>
            </div>
          </div>
        </swiper-slide>
        <swiper-slide v-for="(slider, index) in sliders" :key="index">
          <div class="slider__img">
            <div class="silder s1 container">
              <div class="text">
                <h3 v-html="slider.title"></h3>
                <p v-html="slider.desc"></p>
                <a href="#" class="more button-blue">more</a>
              </div>
              <div class="img" aria-label="hidden">
                <img :src="slider.iconImage7" :alt="slider.title" />
                <img :src="slider.iconImage8" :alt="slider.title" />
                <img :src="slider.iconImage9" :alt="slider.title" />
              </div>
              <div class="circle" aria-label="hidden">
                <span class="circle c1"></span>
                <span class="circle c2"></span>
                <span class="circle c3"></span>
                <span class="circle c4"></span>
                <span class="circle c5"></span>
              </div>
            </div>
          </div>
        </swiper-slide>
      </swiper>

      <!-- //slider__wrap -->
    </div>
  </section>
</template>

<script>
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css";
import "swiper/css/navigation";
import "swiper/css/pagination";
import "swiper/css/scrollbar";

export default {
  data: function () {
    return {
      sliders: [
        {
          title: "<h3>FOR <br />YOGA</h3>",
          desc: "<p>DESIRE<br />IMAGINE/</p>",
          iconImage1: "./assets/images/slider/slider_icon01.png",
          iconImage2: "./assets/images/slider/slider_icon02.png",
          iconImage3: "./assets/images/slider/slider_icon03.png",
        },
        {
          title: "<h3>FOR <br />YOGA</h3>",
          desc: "<p>DESIRE<br />IMAGINE/</p>",
          iconImage4: "./assets/images/slider/slider_icon04.png",
          iconImage5: "./assets/images/slider/slider_icon05.png",
          iconImage6: "./assets/images/slider/slider_icon06.png",
        },
        {
          title: "<h3>FOR <br />YOGA</h3>",
          desc: "<p>DESIRE<br />IMAGINE/</p>",
          iconImage7: "./assets/images/slider/slider_icon07.png",
          iconImage8: "./assets/images/slider/slider_icon08.png",
          iconImage9: "./assets/images/slider/slider_icon09.png",
        },
      ],
    };
  },
  props: {
    attr: String,
  },
  components: {
    Swiper,
    SwiperSlide,
  },
};
</script>

<style lang="scss">
.swiper {
  overflow: visible;
}
.swiper-pagination {
  bottom: -80px !important;
}

.slider__inner {
  position: relative;
  overflow: hidden;

  .slider__img {
    .silder {
      .text {
        h3 {
          font-size: 110px;
          font-weight: 900;
          text-transform: uppercase;
          line-height: 1;
          margin-bottom: 40px;
        }
        p {
          font-size: 24px;
          line-height: 1.2;
          margin-bottom: 50px;
          font-weight: 600;
        }
        .more {
          font-size: 18px;
          font-weight: 500;
        }
      }
      .img {
        width: 600px;
        height: 600px;
        background-image: url(@/assets/images/slider/slider_icon11.png);
        position: absolute;
        top: -120px;
        right: 0;
        background-size: cover;

        img {
          &:nth-child(1) {
            position: absolute;
            width: 300px;
            top: 0;
          }
          &:nth-child(2) {
            position: absolute;
            width: 300px;
            right: 0;
            bottom: 100px;
          }
          &:nth-child(3) {
            position: absolute;
            width: 300px;
            bottom: 20px;
            left: 55px;
          }
        }
      }
      .circle {
        span {
          display: block;
          position: absolute;
          left: 50%;
          top: 50%;
          width: 20px;
          height: 20px;
          border-radius: 50%;
        }
        span:nth-child(1) {
          background-color: var(--button_blue);
          left: 40%;
          width: 10px;
          height: 10px;
        }
        span:nth-child(2) {
          background-color: var(--button_red);
          top: 20%;
          left: -10%;
          width: 40px;
          height: 40px;
        }
        span:nth-child(3) {
          background-color: var(--button_green);
          left: 100%;
          top: 10%;
        }
        span:nth-child(4) {
          background-color: var(--button_red);
          left: 17%;
          top: -10%;
          width: 10px;
          height: 10px;
        }
        span:nth-child(5) {
          background-color: var(--button_blue);
        }
      }
    }
  }
  .slider__btn {
    > a {
      position: absolute;
      top: 50%;
      transform: translateY(-50%);
      width: 22px;
      height: 40px;
      transition: opacity 0.3s;

      &:hover {
        opacity: 0.5;
      }
    }
    .left {
      left: 20px;
      background-image: url(@/assets/images/slider/slider_left.png);
    }
    .right {
      right: 20px;
      background-image: url(@/assets/images/slider/slider_right.png);
    }
  }
  .slider__dot {
    position: absolute;
    left: 50%;
    bottom: -80px;
    transform: translateX(-50%);
    a {
      display: inline-block;
      width: 16px;
      height: 16px;
      border-radius: 50%;
      margin: 0 5px;
      border: 4px solid #ff3344;
      background-color: #ff3344;
      box-shadow: 0 0 0 3px transparent;
      &.active {
        box-shadow: 0 0 0 3px #ff3344;
        border-width: 4px;
        background-color: #fff;
      }
    }
  }
}
</style>
