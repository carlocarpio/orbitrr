<template>
  <div>
    <HeaderNav />
    <div class="items columns1">
      <a href="#" class="column1">
        <div class="item">
          <div class="item-icon-container">
            <img src="~assets/images/icon-launch.png" alt="Launch">
          </div>
          <div class="item-content">
            <p class="item-title">LAUNCH</p>
            <p class="item-description">Launch a new mission or view your existing missions</p>
          </div>
        </div>
      </a>

      <a href="#" class="column1">
        <div class="item">
          <div class="item-icon-container">
            <img src="~assets/images/icon-launch.png" alt="Launch">
          </div>
          <div class="item-content">
            <p class="item-title">CAPTURE</p>
            <p class="item-description">Content Creators can view available missions and pitch</p>
          </div>
          </div>
      </a>

      <a href="#" class="column1">
        <div class="item">
          <div class="item-icon-container">
            <img src="~assets/images/icon-launch.png" alt="Launch">
          </div>
          <div class="item-content">
            <p class="item-title">PITCH</p>
            <p class="item-description">Content Creators can view their existing submissions.</p>
          </div>
        </div>
      </a>

      <a href="#" class="column1">
        <div class="item">
          <div class="item-icon-container">
            <img src="~assets/images/icon-launch.png" alt="Launch">
          </div>
          <div class="item-content">
            <p class="item-title">CONNECT</p>
            <p class="item-description">Users can view their existing matches here.</p>
          </div>
        </div>
      </a>
    </div>
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
  .columns1 {
    display: flex;
    min-height: 100%;
    flex-wrap: wrap;
    flex-direction: row;
  }
  .column1 {
    flex-basis: calc(25% - 40px);
    justify-content: center;
    flex-direction: column;
    display: flex;
    width: 250px
  }
  .item {
    display: flex;
    align-items: center;
    border: 1px solid #FFFFFF;
    border-radius: 3px;
    /* margin: 0 10px; */
    /* width: 20%; */
    max-height: 500px;
    /* padding: 15px; */
  }
  .item-content {
    width: 70%;
    display: none;
  }
  .items {
    /* display: flex; */
    align-items: center;
    justify-content: center;
    /* margin: 0 30px; */
  }
  .item-title {
    color: #36DCBE;
    font-size: 20px;
    font-weight: 900;
  }
  .item-description {
    color: #FFFFFF;
    font-size: 13px;
  }
  .item-icon-container {
    width: 135px;
    height: 135px;
    margin: 0 5px;
    display: flex;
  }
  .item-icon-container img {
    width: 40%;
    height: 50px;
  }
</style>
