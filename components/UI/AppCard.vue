<template>
  <div style="margin-bottom: 2rem">
    <div class="img-container">
      <img :src="getImgUrl(cardObj.imgPath)" />
    </div>

    <div class="title">
      <h5>{{ cardObj.title }}</h5>
    </div>
    <div>
      <h3>{{ cardObj.description }}</h3>
    </div>

    <div
      v-if="!cardObj.badgeList || cardObj.badgeList.length !== 0"
      class="badge"
    >
      <ul>
        <li v-for="(badge, index) in cardObj.badgeList" :key="index">
          {{ badge }}
        </li>
      </ul>
    </div>
  </div>
</template>
<script>
export default {
  name: 'AppCard',
  props: {
    cardObj: {
      type: Object,
      default: () => ({
        badgeList: [],
      }),
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
.img-container {
  @include breakpoint-up(large) {
    height: 25rem;
  }
  img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
}

ul {
  list-style-type: none;
  display: flex;
  flex-wrap: wrap;
  padding: 0;
  margin-top: 1rem;
  li {
    font-family: $nunito;
    font-weight: 700;
    font-size: 14px;
    border: 2px solid $dark-grey;
    box-sizing: border-box;
    border-radius: 8px;
    padding: 0.5rem 1.5rem;
    margin-right: 0.5rem;
    margin-bottom: 0.5rem;
  }
}
.title {
  position: relative;
  color: $gold;
  margin-top: 1.5625rem;
  h5 {
    margin-left: 4.5rem;
  }
  &::before {
    content: '';
    background-image: url('@/assets/img/dashed-arrow.svg');
    background-repeat: no-repeat;
    background-size: contain;
    position: absolute;
    top: 0.25rem;
    bottom: 0;
    height: 1.1875rem;
    width: 5.0625rem;
  }
}
</style>
