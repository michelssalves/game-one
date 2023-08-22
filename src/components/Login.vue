<template>
  <div class="login-container">
    <form @submit.prevent="logon" class="login-form">
      <div class="logo-container">
        <img src="favicon.ico" alt="Logo" class="logo" />
      </div>
      <div class="form-group">
        <label for="username">Usuário</label>
        <input type="text" v-model="username" id="username" class="input-field" required />
      </div>
      <div class="form-group">
        <label for="password">Senha</label>
        <input type="password" v-model="password" id="password" class="input-field" required />
      </div>
      <button type="submit" class="login-button">Login</button>
      <div class="signup-link">
      Ainda não tem uma conta? <a href="/cadastro">Cadastre-se</a>
    </div>
    </form>

  </div>
</template>
  
<script>
export default {
  // eslint-disable-next-line 
  name: 'Login',
  data() {
    return {
      username: '',
      password: ''
    };
  },
  methods: {

    logon() {
      // Simulação de validação de login
      if (this.username === 'usuario' && this.password === 'senha') {

        
        this.$router.push('/home');
        this.$emit('welcome', true); // Emite o evento com acesso válido

      } else {
      
        this.$emit('login-success', true); // Emite o evento com acesso inválido
        if (this.$route.path !== '/') {
        this.$router.push('/');
        }
      }
    }

  }
};
</script>
  
<style scoped>
.login-container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background-color: #f5f5f5; /* Cor de fundo */
}

.login-title {
  font-size: 24px;
  margin-bottom: 20px;
  color: #333; /* Cor do texto */
}

.login-form {
  max-width: 300px;
  width: 100%;
  padding: 20px;
  border: 1px solid #ddd;
  border-radius: 5px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  background-color: #fff; /* Cor de fundo */
}

.form-group {
  margin-bottom: 15px;

}

label {
  display: block;
  font-weight: bold;
  margin-bottom: 5px;
  color: #555; /* Cor do texto */
}
input {
  width: 100%;
  padding: 8px;
  border: 1px solid #ccc;
  border-radius: 3px;
}

.login-button {
  display: block;
  width: 100%;
  padding: 10px;
  background-color: #9e0b0b;
  color: white;
  border: none;
  border-radius: 3px;
  cursor: pointer;
}

.login-button:hover {
  background-color: #7a0a0a;
}

.logo-container {
  display: flex;
  justify-content: center;
  margin-bottom: 20px;
}

.logo {
  max-width: 100px; /* Ajuste o tamanho da logo conforme necessário */
}
.login-button {
  display: block;
  width: 40%; /* Largura do botão */
  margin: 10px auto; /* Centraliza o botão */
  padding: 10px;
  background-color: #007bffe7; /* Cor azul */
  color: white;
  border: none;
  border-radius: 6px;
  cursor: pointer;
}

.login-button:hover {
  background-color: #0056b3; /* Cor azul mais escura no hover */
}

/* Centraliza o botão */
.login-form {
  text-align: center;
}
.input-field {
  width: 80%; /* Ajuste a porcentagem conforme necessário */
  padding: 8px;
  border: 1px solid #ccc;
  border-radius: 6px;
}
.signup-link {
  text-align: center;
  margin-top: 20px;
  font-family:Georgia, 'Times New Roman', Times, serif;
}

.signup-link a {
  color: #007bff; /* Cor azul para o link */
  text-decoration: none;
}

.signup-link a:hover {
  text-decoration: underline;
}
</style>
  