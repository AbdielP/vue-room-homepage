<template>
  <figure class="figure">
    <img
      class="figure__img"
      src="../../public/images/desktop-image-hero-1.jpg"
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
/* div {
        width: 100%;
        height: 400px;
        background: goldenrod;
    } */

.figure {
  width: 100%;
  /* height: 350px; */
  overflow: 'hidden';
}

.figure__img {
    width: 100%;
    height: 100%;
    object-fit: fill;
}
</style>