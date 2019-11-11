<template>
    <div class='header'>
        <nuxt-link class='logo-container' to="/">
            <img class='logo' :src="logo" alt="Logo" />
        </nuxt-link>
        <div class='options'>
            <nuxt-link class='option' to='/shop'>
                SHOP
            </nuxt-link>
            <nuxt-link class='option' to='/contact'>
                CONTACT
            </nuxt-link>
            <nuxt-link class='option' to='/sign-in'>
                SIGN IN
            </nuxt-link>
        </div>
    </div>  
</template>

<script>
import Logo from '../assets/crown.svg';

export default {
    data() {
        return {
            logo: Logo
        }
    }
}
</script>

<style lang="scss">
.header {
    height: 70px;
    width: 100%;
    display: flex;
    justify-content: space-between;
    margin-bottom: 25px;
  
    .logo-container {
      height: 100%;
      width: 70px;
      padding: 25px;
    }
  
    .options {
      width: 50%;
      height: 100%;
      display: flex;
      align-items: center;
      justify-content: flex-end;
  
      .option {
        padding: 10px 15px;
      }
    }
  }
  
</style>