<template>
  <router-view />
</template>

<script>
import Navigation from "./components/Navigation.vue";

export default {
  components: {
    Navigation,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Spartan:wght@500;600;700&display=swap");

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Spartan", sans-serif;

  --color-dark-gray: hsl(0, 0%, 63%);
  --color-black: hsl(0, 0%, 0%);
  --color-white: hsl(0, 0%, 100%);
  --color-very-dark-grey: hsl(0, 0%, 27%);
}

body {
  font-size: 12px;
}

.cursor-pointer {
  cursor: pointer;
}

.info__paragraph {
  color: var(--color-dark-gray);
  margin: 20px 0;
  line-height: 1.7;
}
</style>
