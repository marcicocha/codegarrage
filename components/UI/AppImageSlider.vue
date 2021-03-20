<template>
  <div class="flex-container">
    <div v-for="(img, i) in imageList" :key="i" class="flex-container__item">
      <img :src="getImgUrl(img)" alt="image" />
    </div>
  </div>
</template>
<script>
export default {
  name: 'AppImageSlider',
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
.flex-container {
  display: flex;
  flex-wrap: nowrap;
  flex-direction: row;
  overflow-x: auto;
  scroll-snap-type: x mandatory;
  scroll-behavior: smooth;
  -webkit-overflow-scrolling: touch;
  -ms-overflow-style: -ms-autohiding-scrollbar;
  &__item {
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
}
</style>
