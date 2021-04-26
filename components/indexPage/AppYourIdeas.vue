<template>
  <div class="flex flex-jc-sb flex-wrap card-parent">
    <AppCard
      v-for="(idea, index) in filteredList"
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
  props: {
    isHomePage: {
      type: Boolean,
      default: false,
    },
  },
  data() {
    return {
      ideaList: [
        {
          title: 'fuseErpTitle',
          description: 'fuseErpDescription',
          domain: 'fuseErpDomain',
          badgeList: [
            'uiUxDesign',
            'webDevelopment',
            'devopsCloudService',
            'softwareTesting',
            'applicationSupport',
          ],
          imgPath: 'idea/fuse.svg',
        },
        {
          title: 'teflonHubTitle',
          description: 'teflonHubDescription',
          domain: 'fintechPaymentGateway',
          badgeList: [
            'Code Review and restructuring',
            'applicationSupport',
            'webDevelopment',
            'mobileDevelopment',
            'softwareTesting',
          ],
          imgPath: 'idea/teflonhub.png',
        },
        {
          title: 'simplefianceTitle',
          description: 'simplefianceDescription',
          domain: 'simplefianceDomain',
          badgeList: ['mobileAppDevelopment'],
          imgPath: 'idea/simplefi.png',
        },
        {
          title: 'atlanticTitle',
          description: 'atlanticDescription',
          domain: 'atlanticDomain',
          badgeList: [
            'webApplication',
            'applicationSupport',
            'devopsCloudService',
          ],
          imgPath: 'idea/atlantic-factorial.png',
        },
        {
          title: 'lucroTitle',
          description: 'lucroDescription',
          domain: 'lucroDomain',
          badgeList: [
            'accelerationIncubation',
            'artificialIntelligenceMachineLearning',
            'mobileAppDevelopment',
          ],
          imgPath: 'idea/lucro.png',
        },
        {
          title: 'konsultTitle',
          description: 'konsultDescription',
          domain: 'konsultDomain',
          badgeList: ['accelerationIncubation', 'web'],
          imgPath: 'idea/360Konsult.svg',
        },
        {
          title: 'centricTitle',
          description: 'centricDescription',
          domain: 'fintechPaymentGateway',
          badgeList: ['devsecOPs'],
          imgPath: 'idea/centric.svg',
        },
        {
          title: 'banklessTitle',
          description: 'banklessDescription',
          domain: 'fintechMobileApp',
          badgeList: [
            'accelerationIncubation',
            'webDevelopment',
            'mobileDevelopment',
          ],
          imgPath: 'idea/bankless.png',
        },
      ],
    }
  },
  computed: {
    filteredList() {
      if (this.isHomePage) {
        const filteredArray = this.ideaList.filter((idea, i) => {
          return i <= 3
        })
        return filteredArray
      }
      return this.ideaList
    },
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
