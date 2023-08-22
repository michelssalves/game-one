<template>
  <div>
    <ProductCarrousel/>
  </div>
</template>

<script>
// @ is an alias to /src
//import Home from '@/components/Home.vue'
import ProductCarrousel from '@/components/ProductCarrousel.vue'
//import Products from './ProductsView.vue'  Products,Home,

export default {
  // eslint-disable-next-line
  name: 'HomeView',
  components: {
    ProductCarrousel

  },
  methods: {
    handleLoginSuccess(isValid) {
      this.isCredentialsValid = isValid;
    },

  }
}
</script>
