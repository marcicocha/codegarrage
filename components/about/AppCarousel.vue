<template>
  <Carousel
    :pagination-enabled="false"
    :per-page-custom="[
      [640, 2],
      [1024, 3],
    ]"
  >
    <slide v-for="(img, i) in imageList" :key="i" class="slide">
      <img :src="getImgUrl(img)" />
    </slide>
  </Carousel>
</template>
<script>
import { Carousel, Slide } from 'vue-carousel'

export default {
  name: 'AppCarousel',
  components: {
    Carousel,
    Slide,
  },
  props: {
    imageList: {
      type: Array,
      default: () => [],
    },
  },
  methods: {
    getImgUrl(pic) {
      return require('~/assets/img' + pic)
    },
  },
}
</script>
<style lang="scss" scoped>
.slide {
  width: 14.125rem;
  height: 9.375rem;
  border-radius: 0.25rem;
  margin-right: 1rem;
  flex-shrink: 0;
  @include breakpoint-up(large) {
    width: 30.3125rem;
    height: 20.25rem;
  }
  img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
}
</style>
