<template>
  <div id="app">
    <NavBar></NavBar>
    <HouseMap :deposit="deposit" monthly="monthly"></HouseMap>
  </div>
</template>

<script>
import NavBar from './components/NavBar.vue'
import HouseMap from './components/HouseMap.vue'

export default {
  name: 'App',

  data() {
    return {

    }
  },

  components: {
    NavBar,
    HouseMap
  }
}
</script>

<style>
* {
    margin: 0;
    padding: 0;
    font-family: 'Nanum Gothic', sans-serif;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.navBar {
  border-bottom: solid 1px #999999;
}


</style>
