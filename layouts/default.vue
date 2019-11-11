<template>
  <div>
    <Header />
    <nuxt />
  </div>
</template>

<script>
import Header from '~/components/Header.vue';

export default {
  components: {
    Header
  }
}
</script>

<style>
body {
  font-family: 'Open Sans Condensed';
  padding: 20px 60px;
  margin: 0
}

a {
  text-decoration: none;
  color: black;
}
</style>
