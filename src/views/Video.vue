<template></template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import VideoPlayer from "@/components/Video/VideoPlayer.vue";

@Component({
  components: {
    VideoPlayer
  }
})
export default class Video extends Vue {}
</script>
