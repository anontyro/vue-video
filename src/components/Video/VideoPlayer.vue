<template>
  
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

export default class VideoPlayer extends Vue{
  @Prop() private id!: string;
}
</script>

<style lang="scss" scoped>

</style>
