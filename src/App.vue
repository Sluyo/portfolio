<script setup>
  import { RouterLink, RouterView } from 'vue-router'
  import SideBar from './components/sideBar.vue'
</script>

<template>
  <RouterView />
</template>

<style lang="scss">
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
  }

  body {
    background-image: url("img/background.png");
    background-repeat: repeat;
    margin: 0;
  }

</style>
