<template>
    <Carousel :autoplay="4000" :wrap-around="true">
      <Slide v-for="slide in slides" :key="slide">
        <img :src="slide.imagem" alt=""><p class="legenda">{{slide.texto}}</p>
      </Slide>
    </Carousel>
  </template>
  <script>
  import { defineComponent } from 'vue';
  import { Carousel, Slide } from 'vue3-carousel';
  
  import 'vue3-carousel/dist/carousel.css';
  
  export default defineComponent({
    name: 'AutoplayComponente',
    components: {
      Carousel,
      Slide,
    
    },
    data() {
      return {
        slides: [
          { imagem: '01.jpg', texto:'ola1' },
          { imagem: '02.jpg', texto:'ola3' },
          { imagem: '03.jpg', texto:'ola2' },
          { imagem: '04.jpg', texto:'ola4' },
          // Adicione mais objetos com caminhos para suas imagens
        ],
      };
    },
  });
  </script>
  <style scoped>
  /* Estilos para tornar o carrossel responsivo */
  .legenda{
    display: flex;
    justify-content: center;
    margin-top: 200px;
    margin-right: 400px;
  }
  </style>