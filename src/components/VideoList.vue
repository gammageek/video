<template>
  <ul class="list-group">
   <VideoListItem 
   @videoSelect="onVideoSelect"
    v-for="video in videos"
    :key="video.etag"
    :video="video"
   >
   </VideoListItem>
  </ul>
</template>

<script>
import VideoListItem from './VideoListItem';
export default {
    name: 'VideoList',
    components: {
        VideoListItem
    },
    props: ['videos'],
    methods: {
      onVideoSelect(video) {
        this.$emit('videoSelect', video);
      }
    }
};
</script>

<style>

</style>