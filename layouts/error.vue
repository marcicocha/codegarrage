<template>
  <section class="container padding">
    <div v-if="error.statusCode === 404">
      <h1>Oops!</h1>
      <br />
      <p>The page you are looking for does not exist</p>
    </div>
    <h1 v-else>An error occurred</h1>
    <!-- <br /> -->
    <!-- <NuxtLink to="/">Go to Home page</NuxtLink> -->
  </section>
</template>
<script>
export default {
  props: {
    error: {
      type: Object,
      default: () => {},
    },
  },
}
</script>
<style lang="scss" scoped>
section {
  text-align: center;
}
h1 {
  font-size: 3rem;
}
</style>
