<template>
  <div class="container">
    <h1>Novo Usuario</h1>
    <form>
        <div class="form-group">
            <label for="nome">Nome</label>
            <input type="text" class="form-control">
        </div>
        <div class="form-group">
            <label for="email">E-mail</label>
            <input type="email" class="form-control">
        </div>
        <div class="form-group">
            <label for="senha">Senha</label>
            <input type="password" class="form-control">
        </div>
        <button class="btn btn-primary" type="submit">Salvar</button>
    </form>
  </div>
</template>