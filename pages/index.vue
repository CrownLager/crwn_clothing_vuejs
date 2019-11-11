<template>
  <div class="container">
    <Directory />
  </div>
</template>

<script>
import Directory from '~/components/Directory.vue';

export default {
  components: {
    Directory
  }
} 
</script>

<style lang="scss" scoped>
.container {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 20px 80px;
  }  
</style>
