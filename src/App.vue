<template>
  <!-- <div id="nav">
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </div> -->
  <!-- <navigation/> -->
  <router-view/>
</template>

<script>
import Navigation from './components/Navigation.vue'

export default {
  components: {
    Navigation
  }
}
</script>

<style>

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

/* .app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
} */

</style>
