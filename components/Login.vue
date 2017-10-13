<template>
  <div class="columns wrapper">
    <div class="login-container column is-half-tablet is-one-quarter-desktop is-three-quarters-mobile">
      <div class="logo-container">
        <img class="login-logo" src="~/assets/images/logo.png" alt="Orbitrr" />
      </div>
      <div v-if="activeTab === 'ForgotPassword'"  class="login-tab">
        <div
          class="btn login-tab-button-full active">
          Forgot password
        </div>
      </div>
      <div v-else class="login-tab">
        <button
          @click="onUpdateTab('Login')"
          type="button"
          class="btn login-tab-button"
          v-bind:class="{ active: activeTab === 'Login' }">
          Login
        </button>
        <button
          @click="onUpdateTab('Signup')"
          type="button"
          class="btn login-tab-button"
          v-bind:class="{ active: activeTab === 'Signup' }">
          Signup
        </button>
      </div>
      <div v-if="activeTab === 'Login'" class="login-form-container">
        <form>
          <div class="field">
            <div class="control">
              <input class="input" type="text" placeholder="Username">
            </div>
          </div>
          <div class="field">
            <div class="control">
              <input class="input" type="password" placeholder="Password">
            </div>
          </div>
          <div class="field">
            <button class="btn login-submit" type="submit">Login</button>
          </div>
          <div class="field">
            <a @click="onUpdateTab('ForgotPassword')" class="link-forgot">Forgot your password?</a>
          </div>
        </form>
      </div>  
      <div v-else-if="activeTab === 'Signup'" class="login-form-container">
        <form>
          <div class="field">
            <div class="control">
              <input class="input" type="text" placeholder="Email">
            </div>
          </div>
          <div class="field">
            <div class="control">
              <input class="input" type="password" placeholder="Password">
            </div>
          </div>
          <div class="field">
            <div class="control">
              <input class="input" type="password" placeholder="Password Confirmation">
            </div>
          </div>
          <div class="field">
            <button class="btn login-submit" type="submit">Signup</button>
          </div>
        </form>
      </div> 
      <div v-else class="login-form-container">
        <form>
          <div class="field">
            <div class="control">
              <input class="input" type="text" placeholder="Email">
            </div>
          </div>
          <div class="field">
            <button class="btn login-submit" type="submit">Send Reset Instruction</button>
          </div>
        </form>
      </div>
      <div v-if="activeTab === 'ForgotPassword'" class="login-tab">
        <button
          @click="onUpdateTab('Login')"
          type="button"
          class="btn login-tab-button"
          v-bind:class="{ active: activeTab === 'Login' }">
          Login
        </button>
        <div class="divider"></div>
        <button
          @click="onUpdateTab('Signup')"
          type="button"
          class="btn login-tab-button"
          v-bind:class="{ active: activeTab === 'Signup' }">
          Signup
        </button>
      </div>
    </div>
  </div>
</template>

<script>
import Logo from './Logo.vue'
export default {
  data () {
    return {
      activeTab: 'ForgotPassword'
    }
  },
  components: {
    Logo
  },
  methods: {
    onUpdateTab (value) {
      this.activeTab = value
    }
  }
}
</script>


<style>
  .wrapper {
    width: 100%;
    justify-content: center;
  }
  .btn {
    outline: none;
    border: none;
    cursor: pointer;
  }

  .login-container {
    border-radius: 8px;
    border: 1px solid #ffffff;
    overflow: hidden;
    width: 100%;
    margin: 0 auto;
    padding: 0;
  }
  .login-tab {
    display: flex;
    justify-content: space-around;
    align-items: center;
    position: relative;
  }
  .login-tab-button {
    width: 50%;
    height: 62px;
    background-color: #D8D8D8;
    border: none;
    font-family: 'Nunito Sans', sans-serif;
    font-size: 20px;
    font-weight: 900;
    color: #243C62;
    justify-content: 'center'
  }
  .login-tab-button-full {
    height: 62px;
    background-color: #3DDCC0;
    border: none;
    font-family: 'Nunito Sans', sans-serif;
    font-size: 20px;
    font-weight: 900;
    color: #FFFFFF;
    display: flex;
    width: 100%;
    justify-content: center;
    align-items: center;
  }
  .login-tab-button.active {
    background-color: #3DDCC0;
    color: #FFFFFF;
  }
  .login-tab-button:focus {
    border: none;
  }
  .login-form-container {
    background-color: #FFFFFF;
    padding: 20% 12%;
  }
  .logo-container {
    background-color: #243C62;
    padding: 10px;
    display: flex;
    justify-content: center;
  }
  .login-logo {
    display: flex;
    height: 40px;
  }
  .login-submit {
    background-color: #3DDCC0;
    border-radius: 3px;
    height: 36px;
    font-size: 18px;
    font-weight: 900;
    font-family: 'Nunito Sans';
    color: #FFFFFF;
    width: 100%;
  }
  .link-forgot {
    display: flex;
    justify-content: flex-end;
    color: #243C62;
    font-size: 14px;
    font-weight: 900;
    font-family: 'Nunito Sans';
  }
  .divider {
    width: 1px;
    height: 40px;
    background: #243C62;
    position: absolute;
  }
</style>

