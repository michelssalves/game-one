<template>
    <div class="product-grid">
      <h1 class="tituloGrid">AS MELHORES OFERTAS</h1>
      <product-card v-for="product in products" :key="product.id" :product="product" />
    </div>
  </template>
  
  <script>
  import ProductCard from './ProductCard.vue';
  
  export default {
    components: {
      ProductCard
    },
    props: {
      products: Array
    }
  }
  </script>
  
  <style scoped>
  .product-grid {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 20px;
  }
  
  .tituloGrid {
    color: #EA9A51;
    font-size: 28px;
    text-align: center;
    margin: 10px 0;
  }
  
  /* Adicione media queries para tornar o t�tulo responsivo */
  @media screen and (max-width: 768px) {
    .tituloGrid {
      font-size: 24px;
    }
  }
  
  @media screen and (max-width: 480px) {
    .tituloGrid {
      font-size: 20px;
    }
  }
  </style>
  