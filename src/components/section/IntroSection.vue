<template>
  <section id="introSection" :class="attr">
    <h3 class="blind">커리큘럼 소개</h3>

    <div class="intro__inner container">
      <div class="intro__title">
        <span>frontend</span>
        <h3 v-html="title"></h3>
        <p v-html="desc"></p>
      </div>
      <div class="intro__desc">
        <div v-for="(text, index) in texts" :key="index">
          <h4 :class="'icon-bg' + (index + 1)">{{ text.title }}</h4>
          <p>{{ text.desc }}</p>
        </div>
        <!-- <div>
          <h4 class="icon-bg2">Node.js</h4>
          <p>프론트앤드 과정입니다</p>
        </div>
        <div>
          <h4 class="icon-bg3">Vue.js</h4>
          <p>프론트앤드 과정입니다</p>
        </div>
        <div>
          <h4 class="icon-bg4">Next.js</h4>
          <p>프론트앤드 과정입니다</p>
        </div> -->
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
      title: "프론트앤드<br />과정",
      desc: "프론트앤드 과정입니다",
      texts: [
        {
          title: "React.js",
          desc: "프론트앤드 과정입니다",
        },
        {
          title: "Node.js",
          desc: "프론트앤드 과정입니다",
        },
        {
          title: "Vue.js",
          desc: "프론트앤드 과정입니다",
        },
        {
          title: "Next.js",
          desc: "프론트앤드 과정입니다",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
//intro

.intro__wrap {
}
.intro__inner {
  @include flex-between;
}
.intro__title {
  width: 33%;
  span {
    background-color: #ff3344;
    font-size: 14px;
    padding: 4px 30px 2px;
    color: #fff;
    border-radius: 40px;
    text-transform: uppercase;
    margin-bottom: 10px;
    display: inline-block;
  }
  h3 {
    font-size: 50px;
    font-weight: 700;
    line-height: 1.2;
    margin-bottom: 30px;
  }
  p {
    font-size: 18px;
    line-height: 1.5;
    font-weight: 500;
  }
}
.intro__desc {
  width: 66%;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  > div {
    width: 48%;
    margin-bottom: 40px;

    h4 {
      font-size: 24px;
      margin-bottom: 15px;
    }

    &:nth-child(3) {
      margin-bottom: 0;
    }
    &:nth-child(4) {
      margin-bottom: 0;
    }
  }
}
</style>
