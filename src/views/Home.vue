<template>
  <div class="div__home">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <gallery />
    <shopnow />
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
  components: {
    Gallery,
    Shopnow,
    About,
    // HelloWorld
  },
};
</script>

<style scoped>
.div__home {
  display: grid;
}

@media (min-width: 600px) {
  .div__home {
    grid-template-columns: 1fr 1fr;
    grid-template-rows: 1fr 1fr;
    gap: 0px 0px;
  }

  .component__about {
    /* background-color: #c7fc6e; */
    grid-row-start: 2;
    grid-column-start: 1;

    grid-row-end: 3;
    grid-column-end: 3;
  }
}
/* https://angrytools.com/css-grid/ */
</style>


