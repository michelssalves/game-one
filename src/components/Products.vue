
<template>
    <div class="app">
      <ProductGrid :products="sampleProducts" />
    </div>
  </template>
  
  <script>
  import ProductGrid from './ProductGrid.vue';

  export default {
    components: {
      ProductGrid,  

    },
  }
  </script>
  
  <style>
  .app {
   
    text-align: center;
    padding: 10px;
    background-color:#282A29;
  }
  </style>
  