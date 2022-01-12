<template>
  <div class="container">
    <navigation />
    <figure class="figure">
      <img
        class="figure__img figure__img--mobile"
        :src="mobile_images[image]"
        alt="Furniture images"
      />

      <img
        class="figure__img figure__img--desktop"
        :src="desktop_images[image]"
        alt="Furniture images"
      />
    </figure>
  </div>
</template>

<script>
import * as m1 from "@/assets/images/mobile-image-hero-1.jpg";
import * as m2 from "@/assets/images/mobile-image-hero-2.jpg";
import * as m3 from "@/assets/images/mobile-image-hero-3.jpg";

import * as d1 from "@/assets/images/desktop-image-hero-1.jpg";
import * as d2 from "@/assets/images/desktop-image-hero-2.jpg";
import * as d3 from "@/assets/images/desktop-image-hero-3.jpg";

import Navigation from '@/components/Navigation.vue';

export default {
  name: "Gallery",
  props: ["image"],
  data() {
    return {
      mobile_images: [m1, m2, m3],
      desktop_images: [d1, d2, d3],
      actualImage: 0,
    };
  },
  components: {
    Navigation
  }
};
</script>

<style scoped>
.container {
  width: 100%;
  min-height: 365px;
}

.figure {
  width: 100%;
  height: 100%;
}

.figure__img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.figure__img--desktop {
  display: none;
}

@media (min-width: 700px) {
  .figure__img--desktop {
    display: block;
  }
  .figure__img--mobile {
    display: none;
  }
}
</style>