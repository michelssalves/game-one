
<template>
  <div>
    <div class="carrousel">
      <Carrousel/>
    </div>
    <div class="lista">
      <ProductGrid :products="sampleProducts" />
    </div>
  </div> 
  </template>
  
  <script>
  import ProductGrid from '../components/ProductGrid.vue';
  import Carrousel from '../components/ProductCarrousel.vue';
  export default {
    components: {
      ProductGrid,
      Carrousel
    },
    data() {
      return {
        sampleProducts: [
          {
            id: 1,
            title: 'God of War Hits PS4',
            description: 'Agua Verde - Curitiba/PR',
            price: '60,00',
            image: '05.jpg'
          },
          {
            id: 2,
            title: 'PS4 Slim C/1 Controle',
            description: 'Boa Vista - Curitiba/PR',
            price: '1950,00',
            image: '06.jpg'
          },
          {
            id: 3,
            title: 'Controle PS5',
            description: 'Jd.Flores - Colombo/PR',
            price: '420,00',
            image: '07.jpg'
          },
          {
            id: 4,
            title: 'Halo - Master Chief',
            description: 'Centro - Curitiba/PR',
            price: '180,00',
            image: '08.jpg'
          },
          // Add more products here
        ],
      };
    }
  }
  </script>
  
  <style>
  .lista {

    text-align: center;
    padding: 10px;
    background-color:#282A29;
  
  }
  .carrousel{
    background-color: #EA9A51;
  }
  </style>
  