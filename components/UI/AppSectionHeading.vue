<template>
  <div>
    <h1>{{ title }}</h1>
    <h1 class="section__heading_description">{{ description }}</h1>
  </div>
</template>
<script>
export default {
  name: 'AppSectionHeading',
  props: {
    title: {
      type: String,
      default: '',
    },
    description: {
      type: String,
      default: '',
    },
  },
}
</script>
<style lang="scss" scoped>
div {
  margin-bottom: 1.5rem;
  @include breakpoint-up(large) {
    margin-bottom: 5rem;
  }
}
.section__heading_description {
  color: $gold;
  margin-left: 3rem;
  margin-top: 0.5rem;
  @include breakpoint-up(large) {
    margin-left: 5rem;
  }
}
</style>
