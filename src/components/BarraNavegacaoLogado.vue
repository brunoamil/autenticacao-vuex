<template>
   <ul class="navbar-nav mr-auto" v-if="usuarioEstaLogado">
          <li class="nav-item">
            <router-link class="nav-link" to="/">Home</router-link>
          </li>
          <li class="nav-item">
            <router-link to="/gerentes" class="nav-link">
              Gerentes
            </router-link>
          </li>
          <li class="nav-item">
            <a href="#" class="nav-link" @click.prevent="efeatuarLogout">Logout</a>
          </li>
        </ul>
</template>
<script>
import { logoutMixin } from '@/mixins';

export default {
  mixins: [ logoutMixin ]
};
</script>
