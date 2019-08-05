<template>
  <div id="app">
    
    <SnapGame msg="Welcome to Playing Card Snap"/>
  </div>
</template>

<script>
import SnapGame from './components/SnapGame.vue'

export default {
  name: 'app',
  components: {
    SnapGame
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
