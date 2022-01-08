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

@import url('https://fonts.googleapis.com/css2?family=Spartan:wght@500;600;700&display=swap');

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Spartan', sans-serif;

  --color-dark-gray: hsl(0, 0%, 63%);
  --color-black: hsl(0, 0%, 0%);
  --color-white: hsl(0, 0%, 100%);
  --color-very-dark-grey: hsl(0, 0%, 27%);
}

body {
  font-size: 12px;
}

/* .app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
} */

</style>
