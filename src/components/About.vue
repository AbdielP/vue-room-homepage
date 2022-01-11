<template>
  <section class="container">
    <figure class="container__img">
      <img
        class="about__img"
        src="@/assets/images/image-about-dark.jpg"
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
        src="@/assets/images/image-about-light.jpg"
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
  height: 100%;
}

.about__img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.info__container {
  padding: 45px 27px;
}

.title {
  font-size: inherit;
  letter-spacing: 3px;
  text-transform: uppercase;
}

@media (min-width: 850px) {
  .container {
    grid-template-columns: 1fr 1.3fr 1fr;
    grid-template-rows: 1fr;
  }

  .info__container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 25px 27px;
  }

  .info__paragraph {
    font-size: 10px;
  }
}

@media (min-width: 1200px) {

  .title {
    font-size: 0.8rem;
  }
  .info__container {
    padding: 0 27px 0 27px;
  }

  .info__paragraph {
    font-size: 12px;
  }
}
</style>