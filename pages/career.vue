<template>
  <div>
    <section class="container padding">
      <h6>{{ $t('career-heading') }}</h6>
      <h3 class="column-6">
        {{ $t('career-description') }}
      </h3>
      <br />
      <button class="button">{{ $t('job-opening') }}</button>
    </section>
    <section class="container padding">
      <h2 class="benefit-heading p-tb">{{ $t('benefits') }}</h2>
      <br />
      <div class="p-tb flex flex-wrap">
        <AppCard
          v-for="(benefit, i) in benefitList"
          :key="i"
          :card-obj="benefit"
          class="contact-card"
        />
      </div>
    </section>
  </div>
</template>
<script>
import AppCard from '@/components/contact/AppCard'
export default {
  components: {
    AppCard,
  },

  data() {
    return {
      benefitList: [
        {
          id: '01',
          title: 'benefit1Title',
          description: 'benefit1Description',
        },
        {
          id: '02',
          title: 'benefit2Title',
          description: 'benefit2Description',
        },
        {
          id: '03',
          title: 'benefit3Title',
          description: 'benefit3Description',
        },
        {
          id: '04',
          title: 'benefit4Title',
          description: 'benefit4Description',
        },
        {
          id: '05',
          title: 'benefit5Title',
          description: 'benefit5Description',
        },
      ],
    }
  },
}
</script>
<style lang="scss" scoped>
.contact-card {
  width: 100%;
  margin-bottom: 1rem;
  @include breakpoint-up(large) {
    width: 30%;
    margin-right: 1rem;
  }
}
.benefit-heading {
  position: relative;
  color: $gold;
  &::after {
    content: '';
    position: absolute;
    bottom: 0.5rem;
    left: 0;
    background-image: url('@/assets/img/benefit-arrow.svg');
    background-size: cover;
    background-repeat: no-repeat;
    height: 1.878125rem;
    width: 7.07125rem;
    @include breakpoint-up(large) {
      bottom: 0.5rem;
      height: 3.448125rem;
      width: 12.9375rem;
    }
  }
}
</style>
