<template>
    <div class="playlist-item">
      <h3>{{ song.title }}</h3>
      <p>Artist: {{ song.artist }}</p>
    </div>
  </template>
  
  <script>
  export default {
    props: ['song'],
  };
  </script>
  
  <style scoped>
  .playlist-item {
    padding: 10px;
    border: 1px solid #a829c2;
    border-radius: 5px;
    margin-bottom: 10px;
    text-align: left;
    background-color: #c5a1c5;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  }
  
  .playlist-item h3 {
    margin: 0 0 10px;
  }
  
  .playlist-item p {
    margin: 0;
  }
  </style>
  