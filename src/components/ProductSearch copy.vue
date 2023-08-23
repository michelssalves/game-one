<template>
<div class="search-bar">
    <div class="centered-container">
      <div class="main">
        <input class="search-field" placeholder="Buscar no GAMEONE"/>
      </div>
    </div>
  </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        searchText: '',
      };
    },
    methods: {
      handleSearch() {
        this.$emit('search', this.searchText); // Emita o evento de busca com o texto digitado
      },
    },
  };
  </script>
  
  <style scoped>
.search-bar {
  margin: 5px;
}

.centered-container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100%;
}

.main {
  width: 100%;
  max-width: 300px;
}
.search-field{
    width: 60%;
    height: 25px;
    border-radius: 10px;
    margin-top: 3px;
}
  </style>
  