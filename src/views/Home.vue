<template>
  <div class="div__home">
    <!-- {{actualImage }} -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <gallery v-bind:image="actualImage"/>
    <shopnow @image="actualImage = $event"/>
    <about class="component__about" />
  </div>
</template>

<script>
import Gallery from "../components/Gallery.vue";
import Shopnow from "../components/Shopnow.vue";
import About from "../components/About.vue";
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: "Home",
  data() {
    return {
      actualImage : 0
    }
  },
  components: {
    Gallery,
    Shopnow,
    About,
    // HelloWorld
  }
};
</script>

<style scoped>
.div__home {
  display: grid;
}

@media (min-width: 600px) {
  .div__home {
    grid-template-columns: 1.5fr 1fr;
    /* grid-template-rows: 1fr 1fr; */
    grid-template-rows: 1fr;
  }

  .component__about {
    grid-row-start: 2;
    grid-column-start: 1;

    grid-row-end: 3;
    grid-column-end: 3;
  }
}
</style>


