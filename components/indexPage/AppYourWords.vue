<template>
  <div class="flex flex-jc-sb">
    <div v-for="(word, index) in wordLists" :key="index" class="word">
      <div class="word__image">
        <img :src="getImgUrl(word.imgPath)" />
      </div>
      <!-- <div>
        <h5>{{ word.name }}</h5>
      </div> -->
      <!-- <div class="m-b word__position">
        <p>{{ word.position }}</p>
      </div> -->
      <p>{{ `" ${word.description} "` }}</p>
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
          name: 'Seun Banjo',
          position: 'CTO, HR-ON-WHEELS',
          description:
            'You all have built an excellent solution that has helped us increase our positive reviews online and given our customers the ability to give us valuable feedback. Thank you for your excellent work with us!',
        },
        {
          imgPath: 'teflon-hub.png',
          name: 'Toun Roberts',
          position: 'CO-FOUNDER, TEFLON HUB',
          description:
            'Your timely response, positive attitude to work, and personalized services has really relieved us a lot of technical stress.',
        },
        {
          imgPath: 'lucro.svg',
          name: 'David Omole',
          position: 'CEO, LUCRO',
          description:
            'The company represents among the highest level of development we’ve ever experienced. They have true entrepreneurial spirits and a lot of knowledge about different types of businesses',
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
  margin-bottom: 1.5rem;
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
