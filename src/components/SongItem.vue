<template>
  <div class="song-item">
    <h3>{{ song.title }}</h3>
    <p>Artist: {{ song.artist }}</p>
    <button @click="addToPlaylist">Add to Playlist</button>
  </div>
</template>

<script>
export default {
  props: ['song'],
  methods: {
    addToPlaylist() {
      this.$emit('add-to-playlist', this.song);
    },
  },
};
</script>

<style scoped>
.song-item {
  padding: 10px;
  border: 1px solid #735d74;
  border-radius: 5px;
  margin-bottom: 10px;
  text-align: left;
  background-color: #d1b4c4;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.song-item h3 {
  margin: 0 0 10px;
}

.song-item p {
  margin: 0 0 10px;
}
</style>
