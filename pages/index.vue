<template>
  <div class="wrapper-login">
    <Login />
  </div>
</template>

<script>
import HeaderNav from '~/components/HeaderNav.vue'
import Login from '~/components/Login.vue'
import Logo from '~/components/Logo.vue'
import Sidebar from '~/components/Sidebar.vue'

export default {
  components: {
    HeaderNav,
    Login,
    Logo,
    Sidebar
  }
}
</script>

<style>
  .wrapper-login {
    display: flex;
    height: 100vh;
    justify-content: center;
    align-items: center;
    background: url('~/assets/images/bg.jpeg') no-repeat bottom left;

  }
</style>
