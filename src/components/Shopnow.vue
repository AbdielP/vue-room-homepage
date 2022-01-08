<template>
  <section class="shopnow">
    <div class="container">
      <div class="container__buttons">
        <button class="container__button cursor-pointer" type="button">
          <svg width="14" height="24" xmlns="http://www.w3.org/2000/svg">
            <path
              d="M13 0L1 12l12 12"
              stroke="#FFF"
              fill="none"
              fill-rule="evenodd"
            />
          </svg>
        </button>
        <button class="container__button cursor-pointer" type="button">
          <svg width="14" height="24" xmlns="http://www.w3.org/2000/svg">
            <path
              d="M1 0l12 12L1 24"
              stroke="#FFF"
              fill="none"
              fill-rule="evenodd"
            />
          </svg>
        </button>
      </div>
    </div>

    <div class="info__container">
      <h1 class="title">Discover innovative ways to decorate</h1>
      <p class="info__paragraph">
        We provide unmatched quality, comfort, and style for property owners
        across the country. Our experts combine form and function in bringing
        your vision to life. Create a room in your own style with our collection
        and make your property a reflection of you and what you love.
      </p>
      <div class="shop__container">
        <p class="shop__paragraph">Shop now</p>
        <svg width="40" height="12" xmlns="http://www.w3.org/2000/svg"><path d="M34.05 0l5.481 5.527h.008v.008L40 6l-.461.465v.063l-.062-.001L34.049 12l-.662-.668 4.765-4.805H0v-1h38.206l-4.82-4.86L34.05 0z" fill="#000" fill-rule="nonzero"/></svg>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Shop",
};
</script>

<style scoped>
.container {
  width: 100%;
  position: relative;
  display: flex;
  justify-content: flex-end;
}

.container__buttons {
  position: absolute;
  bottom: 100%;
}

.container__button {
  width: 60px;
  height: 60px;
  border: none;
  background: var(--color-black);
}

.info__container {
  padding: 70px 27px;
}

.title {
  font-size: 1.7rem;
  font-weight: 600;
}

.info__paragraph {
  color: var(--color-dark-gray);
  margin: 20px 0;
  line-height: 1.7;
}

.shop__container {
  display: flex;
  margin-top: 50px;
}

.shop__paragraph {
  margin-right: 40px;
  text-transform: uppercase;
  font-size: .8rem;
  letter-spacing: 10px;
}
</style>