<template>
  <div id="app">
    <TheNavBar/>
    <div class="container">
      <router-view/>
    </div>
  </div>
</template>

<script>
  import TheNavBar from '@/components/TheNavBar'
  export default {
    name: 'app',
    components: {
      TheNavBar
    }
  }
</script>

<style>
  @import url("assets/css/styles.css");
</style>
