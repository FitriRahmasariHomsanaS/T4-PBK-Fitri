<template>
    <div class="cart-item">
      <h3>{{ item.name }}</h3>
      <p>Price: ${{ item.price }}</p>
    </div>
  </template>
  
  <script>
  export default {
    props: ['item'],
  };
  </script>
  
  <style scoped>
  .cart-item {
    padding: 10px;
    border: 1px solid #ac21d6;
    border-radius: 5px;
    margin-bottom: 10px;
    text-align: left;
  }
  
  .cart-item h3 {
    margin: 0 0 10px;
  }
  
  .cart-item p {
    margin: 0;
  }
  </style>
  