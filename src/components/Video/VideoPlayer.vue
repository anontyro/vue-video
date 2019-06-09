<template>
  <div>
    <h3>Video with ID: {{ videoId }}</h3>
    <video ref="mainPlayer" class="video-js"/>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';
import videojs from 'video.js';
import 'video.js/dist/video-js.min.css';
import 'videojs-youtube/dist/Youtube.min.js';

@Component
export default class VideoPlayer extends Vue {
  @Prop() private videoId!: string;
  @Prop() private options!: object;
  player: any;

  data() {
    return {
      player: '',
    };
  }

  mounted() {
    this.setupPlayer();
    console.log(`video id : ${this.videoId}`);
  }

  onPlayerReady(): any {
    console.log('Player ready', this);
  }

  setupPlayer(): any {
    this.player = videojs(this.$refs.mainPlayer, this.options, () =>
      this.onPlayerReady(),
    );
  }

  private beforeDestory() {
    if (this.player) {
      this.player.dispose();
    }
  }
}
</script>

<style lang="scss" scoped>
</style>
