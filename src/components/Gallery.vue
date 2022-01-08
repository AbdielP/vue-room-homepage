<template>
  <figure class="figure">
    <img
      class="figure__img"
      src="../../public/images/mobile-image-hero-1.jpg"
      alt="Furniture images"
    />
  </figure>
</template>

<script>
export default {
  name: "Gallery",
};
</script>

<style scoped>
.figure {
  width: 100%;
  height: 365px;
}

.figure__img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}
</style>