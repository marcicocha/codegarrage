<template>
  <div class="contact__card">
    <div class="styled__h2">
      <h2>{{ cardObj.id }}</h2>
      <span></span>
    </div>

    <h3 class="p-tb">{{ cardObj.title }}</h3>
    <p>{{ cardObj.description }}</p>
  </div>
</template>
<script>
export default {
  name: 'AppCard',
  props: {
    cardObj: {
      type: Object,
      default: () => ({}),
    },
  },
}
</script>
<style lang="scss" scoped>
.contact {
  &__card {
    padding: 1.5rem;
    background: $dark-grey;

    .styled__h2 {
      position: relative;
      margin-left: 1rem;
      margin-top: 1rem;
      h2 {
        position: relative;
        width: fit-content;
        font-weight: 900;
        background: $gold;
        padding-left: 0.25rem;
        padding-right: 0.25rem;
        font-size: 1.25rem;
        border-radius: 0.25rem;
        z-index: 2;
        @include breakpoint-up(large) {
          padding-left: 0.5rem;
          padding-right: 0.5rem;
          font-size: 2rem;
        }
      }
      span {
        position: absolute;
        top: -0.5rem;
        left: -0.5rem;
        height: 100%;
        background-color: $dark-red;
        border-radius: 0.25rem;
        width: 2rem;
        @include breakpoint-up(large) {
          top: -0.8rem;
          left: -0.8rem;
          width: 3.38375rem;
        }
      }
    }
  }
}
</style>
