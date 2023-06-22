<template>
  <div>
    <main>
      <SliderSection attr="slider__wrap section nanum7" />
      <IntroSection attr="intro__wrap section nanum7" />
      <!-- <MemberSection /> -->
      <PortSection attr="port__wrap section nanum7" />
      <MovieSection attr="slider__wrap section nanum7" />
      <YoutubeSection attr="youtube__wrap section nanum7" />
      <UnsplashSection attr="unsplash__wrap section nanum7" />
    </main>
  </div>
</template>

<script>
import SliderSection from "@/components/section/SliderSection.vue";
import IntroSection from "@/components/section/IntroSection.vue";
// import MemberSection from "@/components/section/MemberSection.vue";
import PortSection from "@/components/section/PortSection.vue";
import MovieSection from "@/components/section/MovieSection.vue";
import UnsplashSection from "@/components/section/UnsplashSection.vue";
import YoutubeSection from "@/components/section/YoutubeSection.vue";

export default {
  components: {
    IntroSection,
    // MemberSection,
    MovieSection,
    PortSection,
    SliderSection,
    UnsplashSection,
    YoutubeSection,
  },
};
</script>
