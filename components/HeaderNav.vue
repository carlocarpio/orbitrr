<template>
  <div class="logo-container">
    <div class="logo-header">
      <div class="logo"><img src="~/assets/images/logo.png" alt="Orbitrr" /></div>
      <div @click="test">Menu</div>
    </div>
  </div>
</template>

<script>
  export default {
    methods: {
      test () {
        console.log(1111)
      }
    }
  }
</script>

<style>
.logo {
  max-width: 150px;
  justify-content: center;
  align-items: center;
  display: flex;
}
.logo-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 100%;
  padding: 0 30px;
}
</style>
