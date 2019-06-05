<template>
  <div class="photo-container">
    <div v-for="photo in photos" class="photo">
      <PhotoItem v-bind:photo="photo" />
    </div>
  </div>
</template>

<script>
import PhotoItem from './PhotoItem.vue';

export default {
  name: "Photos",
  components: {
    PhotoItem
  },
  props: ["photos"]
}
</script>

<style scoped>

  .photo-container {
    background: hsla(0,0%,30%,.9);
    display: inline-flex;
    flex-wrap: wrap;
    padding: 10px;
    width: 100%;
  }

  .photo {
    flex: 1 0 21%;
    text-align: center;
    vertical-align: middle;
  }

</style>
