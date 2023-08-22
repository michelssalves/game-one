<template>
  <div>
    <Login :username="username" :password="password" @login-success="handleLoginSuccess"/>
    <div class="msgAcesso">
      <p v-if="isCredentialsValid">Acesso inválido</p>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Login from '@/components/Login.vue'

export default {
  // eslint-disable-next-line
  name: 'LoginView',
  components: {
    Login
  },
  data() {
    return {
      username: '',
      password: '',
      isCredentialsValid: false
    };
  },
  methods: {
    handleLoginSuccess(isValid) {
      this.isCredentialsValid = isValid;
    }
  }
}
</script>
<style>
.msgAcesso{
  background-color: rgb(238, 30, 30);
  display: flex;  
  justify-content: center;
  align-items: center;
  margin-left: 32rem;
  margin-right: 32rem;
  margin-top: 1rem;
  border-radius: 5px;

}
</style>
