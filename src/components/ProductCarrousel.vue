<template>
    <v-carousel :continuous="false" :show-arrows="false" height="300" cycle :interval="3000">
      <v-carousel-item v-for="(slide, i) in slides" :key="i">
        <v-sheet>
          <div class="d-flex fill-height justify-center align-center">
              <img :src="slide.imagem" class="carousel-image">
          </div>
        </v-sheet>
      </v-carousel-item>
    </v-carousel>
</template>
<script>
  export default {
    data () {
      return {
        slides: [
        { imagem: '01.jpg', texto: 'Seja um rei do Crime' },
        { imagem: '02.jpg', texto: 'Brilhe no modo carreira' },
        { imagem: '03.jpg', texto: 'Ta afim de passar raiva, compre esse jogo!' },
        { imagem: '04.jpg', texto: 'A delicinha de todos os tempos, sem arrependimentos!' },
        // Adicione mais objetos com caminhos para suas imagens e legendas
      ],
      }
    },
  }
</script>
<style scoped>

.carousel-image {
  min-width: 100%; /* Ajusta a largura da imagem para o tamanho do slide */
  min-height: 100%;
  object-fit:fill; /* Ajusta o modo de exibição da imagem */
}
.carousel-container {
  height: 300px; /* Define uma altura padrão para o carrossel */
}

@media (max-width: 600px) {
  .v-carousel {
    height: 100vh; /* Define a altura do carrossel para 100% da tela em dispositivos móveis */
  }


  .carousel-container {
    height: 100vh; /* Define a altura do carrossel para 100% da tela em dispositivos móveis */
  }
}
</style>