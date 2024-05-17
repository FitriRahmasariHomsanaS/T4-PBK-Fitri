<template>
  <div class="app">
    <h1>Music Playlist</h1>
    <song-list @add-to-playlist="addToPlaylist"></song-list>
    <playlist :songs="playlistSongs"></playlist>
  </div>
</template>

<script>
import SongList from './components/SongList.vue';
import Playlist from './components/Playlist.vue';

export default {
  components: {
    SongList,
    Playlist,
  },
  data() {
    return {
      playlistSongs: [],
    };
  },
  methods: {
    addToPlaylist(song) {
      this.playlistSongs.push(song);
    },
  },
};
</script>

<style scoped>
.app {
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 10px;
  text-align: center;
  background-color: #f0f0f0;
  max-width: 600px;
  margin: auto;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

button {
  padding: 10px 20px;
  cursor: pointer;
  background-color: #3498db;
  color: #fff;
  border: none;
  border-radius: 5px;
  transition: background-color 0.3s ease;
}

button:hover {
  background-color: #2980b9;
}

h1 {
  font-size: 28px;
  color: #333;
  margin-bottom: 20px;
}
</style>
