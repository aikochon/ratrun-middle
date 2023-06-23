<template>
  <carousel :items-to-show="1">
    <Slide v-for="(image, key) in images" :key="key">
      <img :src="getImg(image)" alt="" />
    </Slide>

    <template #addons>
      <!-- <button
        @click="clickImg(key slide to)"
        v-for="(image, key) in images"
        :key="key"
      >
        <img :src="getImg(image)" alt="" />
      </button> -->
      <navigation />
      <pagination />
    </template>
  </carousel>
</template>
  
  <script>
// If you are using PurgeCSS, make sure to whitelist the carousel CSS classes
import "vue3-carousel/dist/carousel.css";
import { Carousel, Slide, Pagination, Navigation } from "vue3-carousel";

export default {
  name: "App",
  components: {
    Carousel,
    Slide,
    Pagination,
    Navigation,
  },
  props: {
    images: {
      type: Array,
      default: null,
    },
  },
  setup() {
    const getImg = (file) => {
      return new URL(`../../../assets/img/${file}`, import.meta.url).href;
    };
    return {
      getImg,
    };
  },
};
</script>
<style lang="scss" scoped>
img {
  height: 300px;
  width: 500px;
  margin: 0 auto;
  @include mobile {
    width: 100%;
    height: auto;
  }
}
</style>
  