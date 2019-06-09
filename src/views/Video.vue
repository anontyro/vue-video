<template>
  <div class="video-page">
    <h3>Vue Video</h3>
    <VideoPlayer :videoId="this.$route.params.id"/>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import VideoPlayer from '@/components/Video/VideoPlayer.vue';

@Component({
  components: {
    VideoPlayer,
  },
})
export default class Video extends Vue {}
</script>
