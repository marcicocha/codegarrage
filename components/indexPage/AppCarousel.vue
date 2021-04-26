<template>
  <Carousel
    :pagination-enabled="false"
    :per-page-custom="[
      [640, 2],
      [1024, 4],
    ]"
  >
    <slide v-for="(img, i) in imageList" :key="i" class="slide">
      <div>
        <img :src="getImgUrl(img.imgPath)" />
      </div>
      <p class="name">{{ img.name }}</p>
      <p class="description">{{ $t(img.description) }}</p>
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
      return require('~/assets/img/' + pic)
    },
  },
}
</script>
<style lang="scss" scoped>
.slide {
  width: 14.125rem;
  height: 17rem;
  border-radius: 0.25rem;
  margin-right: 1rem;
  flex-shrink: 0;
  @include breakpoint-up(large) {
    width: 30.3125rem;
    height: 30.25rem;
  }
  @include breakpoint-up(xxlarge) {
    width: 30.3125rem;
    height: 50.25rem;
  }
  div {
    width: 100%;
    height: 60%;
    img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      object-position: top;
      border-radius: 0.625rem;
    }
  }
}
.description {
  font-family: $nunito;
  font-weight: 700;
  font-size: 14px;
  border: 2px solid $dark-grey;
  box-sizing: border-box;
  border-radius: 8px;
  padding: 0.1rem 0.5rem;
  margin-top: 0.5rem;
  width: fit-content;
  @include breakpoint-down(medium) {
    font-size: 0.75rem;
  }
}
.name {
  font-size: 1rem;
  font-weight: 700;
  margin-top: 1rem;
  @include breakpoint-up(large) {
    font-size: 1.25rem;
  }
}
</style>
