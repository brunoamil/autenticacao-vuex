<template>
  <div class="container">
    <h1>Login </h1>
    <form @submit.prevent="efetuarLogin">
      <div class="form-group">
        <label for="email">E-mail</label>
        <input type="email" class="form-control" v-model="usuario.email">
      </div>
      <div class="form-group">
        <label for="senha">Senha</label>
        <input type="password" class="form-control" v-model="usuario.senha">
      </div>
      <button type="submit" class="btn btn-primary btn-block">Logar</button>
      <router-link :to="{ name: 'novo.usuario' }">Não possui um cadastro</router-link>
    </form>
  </div>
</template>
<script>

export default {
  data () {
    return {
      usuario: {}
    };
  },
  methods: {
    efetuarLogin(){
      this.$http.post('auth/login', this.usuario)
      .then(response => {
        console.log(response);
        localStorage.setItem('token', response.data.acesses_token);
        this.$router.push({name: 'gerentes'});
      })
      .catch(erro => console.log(erro));
    }
  }
};
</script>
