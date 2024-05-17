<template>
  <div class="playlist">
    <h2>Your Playlist</h2>
    <playlist-item
      v-for="(song, index) in songs"
      :key="index"
      :song="song"
    ></playlist-item>
    <p v-if="songs.length === 0">Your playlist is empty.</p>
  </div>
</template>

<script>
import PlaylistItem from './PlaylistItem.vue';

export default {
  components: {
    PlaylistItem,
  },
  props: ['songs'],
};
</script>

<style scoped>
.playlist {
  margin: 20px 0;
}

.playlist h2 {
  font-size: 22px;
  margin-bottom: 15px;
}

.playlist p {
  color: #ce22d4;
}
</style>
