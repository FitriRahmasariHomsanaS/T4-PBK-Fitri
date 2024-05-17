<template>
  <div class="song-list">
    <h2>Available Songs</h2>
    <song-item
      v-for="song in songs"
      :key="song.id"
      :song="song"
      @add-to-playlist="handleAddToPlaylist"
    ></song-item>
  </div>
</template>

<script>
import SongItem from './SongItem.vue';

export default {
  components: {
    SongItem,
  },
  data() {
    return {
      songs: [
        { id: 1, title: 'Spring Day', artist: 'BTS' },
        { id: 2, title: 'Favorite Girl', artist: 'Justin Bieber' },
        { id: 3, title: 'Tak segampang itu', artist: 'Anggi Marito' },
      ],
    };
  },
  methods: {
    handleAddToPlaylist(song) {
      this.$emit('add-to-playlist', song);
    },
  },
};
</script>

<style scoped>
.song-list {
  margin: 20px 0;
}

.song-list h2 {
  font-size: 22px;
  margin-bottom: 15px;
}
</style>
