<template>
  <div class="service-card">
    <div class="child-container">
      <div class="title">
        <h5>{{ $t(cardObj.title) }}</h5>
      </div>
      <p>{{ $t(cardObj.description) }}</p>
      <div
        v-if="!cardObj.badgeList || cardObj.badgeList.length !== 0"
        class="badge"
      >
        <ul>
          <li v-for="(badge, index) in cardObj.badgeList" :key="index">
            {{ $t(badge) }}
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'AppServiceCard',
  props: {
    cardObj: {
      type: Object,
      default: () => ({
        badgeList: [],
      }),
    },
  },
}
</script>
<style lang="scss" scoped>
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
    width: 4.5rem;
  }
}
.service-card {
  margin-bottom: 1rem;
  .child-container {
    width: 100%;
    @include breakpoint-up(large) {
      width: 80%;
    }
  }
  @include breakpoint-up(large) {
    &:nth-child(even) {
      .child-container {
        float: right;
      }
    }
  }
}
</style>
