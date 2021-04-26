<template>
  <div>
    <section class="container padding">
      <h6>{{ $t('whatWeOffer') }}</h6>
      <h3 class="column-6" style="margin-bottom: 2rem">
        {{ $t('servicesDescription') }}
      </h3>
      <br />
      <div class="service-img">
        <img
          src="@/assets/img/idea/atlantic-factorial.png"
          alt="atlantic-factorial"
        />
      </div>
    </section>
    <section class="container padding">
      <div class="flex flex-jc-sb flex-wrap">
        <AppServiceCard
          v-for="(card, i) in cardList"
          :key="i"
          :card-obj="card"
          class="column-6 card"
        />
      </div>
    </section>
  </div>
</template>
<script>
import AppServiceCard from '@/components/service/AppServiceCard'
export default {
  components: {
    AppServiceCard,
  },

  data() {
    return {
      cardList: [
        {
          title: 'webDevelopment',
          description: 'webDevelopmentDescription',
          badgeList: ['frontend', 'backend'],
        },
        {
          title: 'mobileDevelopment',
          description: 'mobileDevelopmentDescription',
          badgeList: ['hybridApp', 'nativeApp'],
        },
        {
          title: 'incubationAccelaration',
          description: 'incubationAccelarationDescription',
          badgeList: ['incubation', 'acceleration'],
        },
        {
          title: 'softwareTestingQA',
          description: 'softwareTestingQADescription',
          badgeList: ['automated', 'manual', 'performance', 'security'],
        },
        {
          title: 'applicationSupport',
          description: 'applicationSupportDescription',
          badgeList: ['maintenance', 'upgrade', 'support'],
        },
        {
          title: 'researchDevelopment',
          description: 'researchDevelopmentDescription',
          badgeList: ['researchLab', 'researchFinding', 'reporting'],
        },
        {
          title: 'cloudEnterprise',
          description: 'cloudEnterpriseDescription',
          badgeList: [
            'erp',
            'crm',
            'hr',
            'accounting',
            'supplyChain',
            'logistics',
          ],
        },
        {
          title: 'devopsService',
          description: 'devopsServiceDescription',
          badgeList: ['devops', 'cloudops'],
        },
        {
          title: 'uiUxProductDesign',
          description: 'uiUxProductDesignDescription',
          badgeList: ['uiUx', 'productDesign', 'branding'],
        },
        {
          title: 'emergencyResponse',
          description: 'emergencyResponseDescription',
          badgeList: ['support', 'development', 'management'],
        },
        {
          title: 'dataAnalytics',
          description: 'dataAnalyticsDescription',
          badgeList: ['ai', 'ml', 'dataAnalytics', 'bots', 'chatbots'],
        },
        {
          title: 'softwareProgramming',
          description: 'softwareProgrammingDescription',
          badgeList: ['internship', 'training', 'consultation'],
        },
      ],
    }
  },
}
</script>
<style lang="scss" scoped>
.service-img {
  width: 100%;
  height: 15rem;
  @include breakpoint-up(large) {
    height: 30.1875rem;
  }
  img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
}
</style>
