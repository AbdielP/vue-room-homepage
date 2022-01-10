<template>
  <figure class="figure">
    <img
      class="figure__img"
      :src="mobile_images[0]"
      alt="Furniture images"
    />
    {{image}}
  </figure>
  <!-- <img v-bind:src="bro" alt="bro.."> -->
  <!-- <p>
    {{mobile_images[0]}}
  </p> -->
</template>

<script>
import * as m1 from '@/assets/images/mobile-image-hero-1.jpg';
import * as m2 from '@/assets/images/mobile-image-hero-2.jpg';
import * as m3 from '@/assets/images/mobile-image-hero-3.jpg';

export default {
  name: "Gallery",
  inject: ['image'],
  data() {
    return {
      mobile_images: [m1,m2,m3]
    };
  },
  created() {
    console.log(`Desde Home: ${this.image}...`)
  }
};
</script>

<style scoped>
.figure {
  width: 100%;
  min-height: 365px;
}

.figure__img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>