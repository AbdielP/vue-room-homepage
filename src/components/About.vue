<template>
  <section class="container">
    <figure class="container__img">
      <img
        class="about__img"
        src="../../public/images/image-about-dark.jpg"
        alt="chairs"
      />
    </figure>
    <div class="info__container">
      <h2 class="title">About our furniture</h2>
      <p class="info__paragraph">
        Our multifunctional collection blends design and function to suit your
        individual taste. Make each room unique, or pick a cohesive theme that
        best express your interests and what inspires you. Find the furniture
        pieces you need, from traditional to contemporary styles or anything in
        between. Product specialists are available to help you create your dream
        space.
      </p>
    </div>

    <figure class="container__img">
      <img
        class="about__img"
        src="../../public/images/image-about-light.jpg"
        alt="chair"
      />
    </figure>
  </section>
</template>

<script>
export default {
  name: "about",
};
</script>

<style scoped>
.container {
  display: grid;
}

.container__img {
  width: 100%;
}

.about__img {
  width: 100%;
  height: 100%;
}

.info__container {
  padding: 45px 27px;
}

.title {
    font-size: inherit;
    letter-spacing: 3px;
    text-transform: uppercase;
}
</style>