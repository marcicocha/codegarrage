<template>
  <div class="flex flex-jc-sb flex-wrap card-parent">
    <AppCard
      v-for="(idea, index) in ideaList"
      :key="index"
      :card-obj="idea"
      class="card"
    />
  </div>
</template>
<script>
import AppCard from '@/components/UI/AppCard'
export default {
  name: 'AppYourNeed',
  components: {
    AppCard,
  },
  data() {
    return {
      ideaList: [
        {
          title: '386Konsult',
          description: 'High-Level Industry Knowledge and Cutting Technology',
          badgeList: ['Branding', 'UI/UX Design'],
          imgPath: 'idea/360Konsult.svg',
        },
        {
          title: 'Driveme NG',
          description:
            'Search, Hire and Manage Verified and Professional Drivers',
          badgeList: ['UI/UX Design', 'Web App Development'],
          imgPath: 'idea/driveMe.svg',
        },
        {
          title: 'Centric Gateway',
          description: 'Building payments into business value chain.',
          badgeList: ['DevsecOPs'],
          imgPath: 'idea/centric.svg',
        },
        {
          title: 'Fuse ERP',
          description: 'Unlock the full potential of your business.',
          badgeList: ['UI/UX Design', 'Web App Development'],
          imgPath: 'idea/fuse.svg',
        },
      ],
    }
  },
}
</script>
<style lang="scss" scoped>
.ideaSection {
  position: relative;
  &::after {
    content: '';
    position: absolute;
    bottom: -1.5rem;
    background-image: url('@/assets/img/idea-arrow.svg');
    background-size: cover;
    background-repeat: no-repeat;
    height: 1.72125rem;
    width: 10.6875rem;
    margin-left: 3rem;
    @include breakpoint-up(large) {
      bottom: -4rem;
      height: 4.548125rem;
      width: 28.245625rem;
      margin-left: 5rem;
    }
  }
}
.card {
  width: 100%;
  margin-bottom: 3rem;
  @include breakpoint-up(large) {
    width: 47%;
    margin-bottom: 4rem;
  }
}
.card-parent {
  margin-top: 3rem;
  @include breakpoint-up(large) {
    margin-top: 7rem;
  }
}
</style>
