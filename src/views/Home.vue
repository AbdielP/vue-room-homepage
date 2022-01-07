<template>
  <div class="home">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <gallery/>
    <shopnow/>
    <about/>
  </div>
</template>

<script>
import Gallery from '../components/Gallery.vue'
import Shopnow from '../components/Shopnow.vue'
import About from '../components/About.vue'
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  components: {
    Gallery,
    Shopnow,
    About
    // HelloWorld
  }
}
</script>
