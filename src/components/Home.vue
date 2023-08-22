<template>
    <div class="Home">
      <h2>Ola Mundo</h2>
    </div>
</template>
  
  <script>
  export default {
    // eslint-disable-next-line 
    name: 'Login',
    props: {
      username: String,
      password: String
    },
    methods: {
      logon() {
        // Lógica de início de sessão aqui
      },

    }
  };
  </script>
  
  <style scoped>
  .login-container {
    max-width: 300px;
    margin: auto;
    padding: 20px;
    border: 1px solid #ccc;
    border-radius: 5px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  }
  
  .form-group {
    margin-bottom: 15px;
  }
  
  label {
    display: block;
    margin-bottom: 5px;
  }
  
  input {
    width: 100%;
    padding: 8px;
    border: 1px solid #ccc;
    border-radius: 3px;
  }
  </style>
  