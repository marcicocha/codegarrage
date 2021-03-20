<template>
  <div class="flex flex-jc-sb">
    <div v-for="(word, index) in wordLists" :key="index" class="word">
      <div class="word__image">
        <img :src="getImgUrl(word.imgPath)" />
      </div>
      <div>
        <h5>{{ word.name }}</h5>
      </div>
      <div class="m-b word__position">
        <p>{{ word.position }}</p>
      </div>
      <p>{{ word.description }}</p>
    </div>
  </div>
</template>
<script>
export default {
  name: 'AppYourWords',
  components: {},
  data() {
    return {
      wordLists: [
        {
          imgPath: 'hr-on-wheels.svg',
          name: 'Azeez Habeeb',
          position: 'CTO, HR-ON-WHEELS',
          description:
            'Our software engineers build high-quality solutions while utilizing the most recent tech capabilities. The range of our services is wide as we have a tech stack that would satisfy all the possible modern requirements of the IT business.',
        },
        {
          imgPath: 'centric.svg',
          name: 'Azeez Habeeb',
          position: 'CO-FOUNDER, CENTRIC GATEWAY',
          description:
            'Our software engineers build high-quality solutions while utilizing the most recent tech capabilities. The range of our services is wide as we have a tech stack that would satisfy all the possible modern requirements of the IT business.',
        },
        {
          imgPath: 'drive-me.svg',
          name: 'Azeez Habeeb',
          position: 'CEO, DRIVEME FLEET SERVICES',
          description:
            'Our software engineers build high-quality solutions while utilizing the most recent tech capabilities. The range of our services is wide as we have a tech stack that would satisfy all the possible modern requirements of the IT business.',
        },
      ],
    }
  },
  methods: {
    getImgUrl(pic) {
      return require('~/assets/img/testimonial/' + pic)
    },
  },
}
</script>
<style lang="scss" scoped>
.word {
  background: $dark-grey;
  border-radius: 5px;
  padding: 1.5rem;
  width: 100%;
  margin-bottom: 1rem;
  @include breakpoint-up(large) {
    width: 32%;
  }
  &__image {
    margin-bottom: 2.4375rem;
  }
  &__position {
    position: relative;
    p {
      margin-left: 3.2rem;
    }
    &::before {
      content: '';
      background-image: url('@/assets/img/dashed-arrow.svg');
      background-repeat: no-repeat;
      position: absolute;
      top: 0.25rem;
      bottom: 0;
      height: 0.875rem;
      width: 2.875rem;
    }
  }
}
</style>
