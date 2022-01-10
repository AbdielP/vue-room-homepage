<template>
  <section class="shopnow">
    <div class="container">
      <div class="container__buttons">
        <button class="container__button cursor-pointer" type="button" v-on:click="galleryBackward()">
          <svg width="14" height="24" xmlns="http://www.w3.org/2000/svg">
            <path
              d="M13 0L1 12l12 12"
              stroke="#FFF"
              fill="none"
              fill-rule="evenodd"
            />
          </svg>
        </button>
        <button class="container__button cursor-pointer" type="button" v-on:click="galleryForward()">
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
      <h1 class="title">{{title}}</h1>
      <p class="info__paragraph">{{text}}</p>
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
  data() {
    return {
      title: "",
      text: "",
      currentInfo: 0,
      info: [
        { title: "Discover innovative ways to decorate", text: "We provide unmatched quality, comfort, and style for property owners across the country. Our experts combine form and function in bringing your vision to life. Create a room in your own style with our collection and make your property a reflection of you and what you love." },
        { title: "We are available all across the globe", text: "With stores all over the world, it's easy for you to find furniture for your home or place of business. Locally, we’re in most major cities throughout the country. Find the branch nearest you using our store locator. Any questions? Don't hesitate to contact us today." },
        { title: "Manufactured with the best materials", text: "Our modern furniture store provide a high level of quality. Our company has invested in advanced technology to ensure that every product is made as perfect and as consistent as possible. With three decades of experience in this industry, we understand what customers want for their home and office." }
      ]
    }
  },
  created() {
    this.initData();
  },
  methods: {
    initData: function () {
      this.title = this.info[0].title;
      this.text = this.info[0].text;
    },
    galleryBackward: function () {
      if (this.currentInfo > 0) {
        this.currentInfo --;
        this.changeInfo(this.currentInfo);
      }
    },
    galleryForward: function() {
      if (this.currentInfo < this.info.length -1) {
        this.currentInfo ++;
        this.changeInfo(this.currentInfo);
      }
    },
    changeInfo: function (value) {
      this.title = this.info[value].title;
      this.text = this.info[value].text;
      // console.log(this.currentInfo);
      // https://blog.logrocket.com/how-to-make-provide-inject-reactive/
      this.$emit('image', this.currentInfo);
    }
  }
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