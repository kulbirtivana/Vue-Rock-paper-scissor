<template>
  <div id="app">
    <h1>Vue Rock Paper Scissors
    </h1>
    <RockPaperScissor />

  </div>
</template>

<script>
import RockPaperScissor from './components/RockPaperScissor.vue'

export default {
  name: 'App',
  components: {
    RockPaperScissor
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
