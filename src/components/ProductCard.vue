<template>
    <div class="product-card">
      <div class="product-image">
        <img :src="product.image" alt="Product Image" class="rounded-image">
      </div>
      <div class="product-details">
        <h3 class="produtoAnuncio">{{ product.title }}</h3>
        <strong class="precoAnuncio">R$ {{ product.price }}</strong>
        <p class="localizacaoAnuncio">{{ product.description }}</p>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      product: Object
    }
  }
  </script>
  
  <style scoped>
  .product-card {
    background: #3F3F3F;
    display: flex;
    align-items: center;
    border: 1px solid #000000;
    padding: 1px;
    margin: 3px;
    border-radius: 10px;
    width: 100%;
  }
  
  .product-image {
    flex: 0.2; /* Reduzindo o espaço ocupado pela imagem */
    width: 60px; /* Reduzindo a largura da imagem */
    margin-right: 10px;
  }
  
  .product-image img {
    max-width: 100%;
    height: auto;
    border-radius: 50%;
    display: block;
  }
  
  .product-details {
    flex: 0.8; /* Aumentando a largura da descrição */
    text-align: left;
    overflow: hidden;
  }
  
  .precoAnuncio {
    color: #EA9A51;
    font-size: 20px;
  }
  
  .produtoAnuncio {
    color: #ffffff;
    font-size: 20px;
    margin: 1px;
    margin-bottom: 20px; /* Reduzindo o espaçamento entre título e preço */
    overflow: hidden;
    white-space: nowrap;
    text-overflow: ellipsis;
  }
  
  .localizacaoAnuncio {
    color: #ffffff;
    font-size: 15px;
    margin-top: 20px; /* Reduzindo o espaçamento entre título e descrição */
    overflow: hidden;
    white-space: nowrap;
    text-overflow: ellipsis;
  }
  </style>
  
  <style scoped>
  @media (min-width: 768px) {
    .product-card {
      padding: 10px;
      max-width: 500px;
    }
  
    .produtoAnuncio {
      font-size: 24px; /* Reduzindo um pouco mais a fonte do título em telas maiores */
      margin-bottom: 30px;
    }
  
    .localizacaoAnuncio {
      font-size: 18px; /* Reduzindo a fonte da descrição em telas maiores */
      margin-top: 40px; /* Reduzindo o espaçamento entre título e descrição */
    }
  }
  </style>
  