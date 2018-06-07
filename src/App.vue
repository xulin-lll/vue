<template>
  <div id="app">
    <gismap></gismap>
  </div>
</template>

<script>
import gismap from './components/gis'
export default {
  name: 'App',
  components:{
    'gismap':gismap
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
