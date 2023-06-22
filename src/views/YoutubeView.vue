<template>
  <div>
    <main>
      <ContTitle title="youtube" />
      <YoutubeSearch />
      <YoutubeSlider />
      <YoutubeTag />
      <YoutubeCont :youtube="youtubes" />
    </main>
  </div>
</template>

<script>
import ContTitle from "@/components/layout/ContTitle.vue";
import YoutubeSearch from "@/components/youtube/YoutubeSearch.vue";
import YoutubeSlider from "@/components/youtube/YoutubeSlider.vue";
import YoutubeTag from "@/components/youtube/YoutubeTag.vue";
import YoutubeCont from "@/components/youtube/YoutubeCont.vue";
import { ref } from "vue";

export default {
  components: {
    ContTitle,
    YoutubeSearch,
    YoutubeSlider,
    YoutubeTag,
    YoutubeCont,
  },

  setup() {
    const youtubes = ref([]);

    const TopYoutubes = async () => {
      await fetch(
        "https://youtube.googleapis.com/youtube/v3/search?part=snippet&maxResults=30&q=%EC%9A%94%EA%B0%80&type=video&key=AIzaSyC7IuUdR0GtIu-4xhJlbkT86HaUTd6_Cgc"
      )
        .then((response) => response.json())
        .then((result) => {
          console.log(result.results);
          youtubes.value = result.results;
        })
        .catch((error) => console.log("error", error));
    };
    TopYoutubes();

    return {
      youtubes,
      TopYoutubes,
    };
  },
};
</script>
