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
          title: 'Fuse ERP',
          description: 'Unlock the full potential of your business',
          domain: 'Enterprise Resource Planning Solution',
          badgeList: [
            'UI/UX Design',
            'Web Development',
            'Devops and Cloud Services',
            'Software Testing/QA',
            'Application Maintenance and Support',
          ],
          imgPath: 'idea/fuse.svg',
        },
        {
          title: 'Teflon Hub',
          description:
            'Payment service provider that allows payment across platforms',
          domain: 'Fintech / Payment Gateway',
          badgeList: [
            'Code Review and restructuring',
            'Application Maintenance and Support',
            'Web Development',
            'Mobile Development',
            'Software Testing/QA',
          ],
          imgPath: 'idea/teflonhub.png',
        },
        {
          title: 'Simplefiance Nigeria',
          description: 'Your business bank on the go',
          domain: 'Fintech / Loan',
          badgeList: ['Mobile App Development'],
          imgPath: 'idea/simplefi.png',
        },
        {
          title: 'Atlantica',
          description:
            'Satellite imagery, aerial data for geospatial solutions',
          domain: 'Remote Sensing / Geospatial Solution',
          badgeList: [
            'Web Application',
            'Application Maintenance and Support',
            'Devops and Cloud Services',
          ],
          imgPath: 'idea/atlantic-factorial.png',
        },
        {
          title: 'Lucro',
          description: 'AI driven investment, payment and advisory platform',
          domain: 'Fintech / Investment / AI',
          badgeList: [
            'Acceleration and Incubation',
            'Artificial Intelligence/Machine Learning',
            'Mobile App Development',
          ],
          imgPath: 'idea/lucro.png',
        },
        {
          title: '386Konsult',
          description: 'Provider of Technology Point in Africa',
          domain: 'Innovation / Technology / consulting / Cybersecurity',
          badgeList: ['Acceleration and Incubation', 'Web'],
          imgPath: 'idea/360Konsult.svg',
        },
        {
          title: 'Centric Gateway',
          description: 'Building payments into business value chain.',
          domain: 'Fintech / Payment Gateway',
          badgeList: ['DevsecOPs'],
          imgPath: 'idea/centric.svg',
        },
        {
          title: 'Bankless',
          description: 'Next-generation Payment Solutions Provider',
          domain: ' Fintech / Mobile app',
          badgeList: [
            'Acceleration and Incubation',
            'Web Development',
            'Mobile Development',
          ],
          imgPath: 'idea/bankless.png',
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
