<template>
  <div class="container">
  <Carousel :autoplay="4000" :wrap-around="true">
    <Slide v-for="(slide, index) in slides" :key="index">
      <div class="slide-content">
        <img :src="slide.imagem" alt="">
        <p class="legenda">{{ slide.texto }}</p>
      </div>
    </Slide>
  </Carousel>
</div>
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
        { imagem: '01.jpg', texto: 'Seja um rei do Crime' },
        { imagem: '02.jpg', texto: 'Brilhe no modo carreira' },
        { imagem: '03.jpg', texto: 'Ta afim de passar raiva, compre esse jogo!'},
        { imagem: '04.jpg', texto: 'A delicinha de todos os tempos, sem arrependimentos!' },
        // Adicione mais objetos com caminhos para suas imagens e legendas
      ],
    };
  },
});
</script>

<style scoped>
/* Estilos para tornar o carrossel responsivo */

.slide-content {
  background-color:#282A29;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  margin-top: 50px;
  padding: 10px;
  margin-bottom: 10px;
  height: auto;
}
.slide-image {
  width: 80%; /* Ajuste a largura da imagem conforme necessário */
  max-width: 600px; /* Defina um valor máximo para a largura da imagem */
  height: auto; /* Mantenha a proporção da imagem */
}

.legenda {
  color: #EA9A51;
  margin-top: 10px;
  cursor: pointer;
  max-height: 3em; /* Defina a altura máxima da legenda em número de linhas */
  overflow: hidden; /* Esconda o conteúdo excedente */
  text-overflow: ellipsis; /* Adicione reticências (...) caso o texto seja cortado */
  white-space: normal; /* Permite a quebra de linha no texto */
}
</style>
