<template>
  <div id="app">
    <the-header />
    <home-page msg=""/>
  </div>
</template>

<script>
import TheHeader from '@/components/organisms/TheHeader.vue'
import HomePage from './pages/HomePage.vue'

export default {
  name: 'App',
  components: {
    TheHeader,
    HomePage
  }
}
</script>

<style>
html {
  touch-action: manipulation;
  max-height: 100vh;
}
body {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  user-select: none;
}
</style>
