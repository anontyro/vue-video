<template>
  <div class="video-page">
    <h3>Vue Video</h3>
    <VideoPlayer :videoId="this.$route.params.id" :options="videoOptions"/>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import VideoPlayer from '@/components/Video/VideoPlayer.vue';

@Component({
  components: {
    VideoPlayer,
  },
  data() {
    return {
      videoOptions: {
        autoplay: true,
        controls: true,
        sources: [
          {
            src: 'https://www.youtube.com/watch?v=N3ugtRtZE0s',
            type: 'video/youtube',
          },
        ],
      },
    };
  },
})
export default class Video extends Vue {}
</script>
