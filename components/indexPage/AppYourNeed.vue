<template>
  <section class="container padding">
    <AppSectionHeading
      class="needSection"
      title="yourNeed"
      description="ourServices"
    />
    <br />
    <div class="hide-for-desktop">
      <AppAccordion
        v-for="need in needList"
        :key="need.id"
        :heading="need.title"
        :init-is-true="false"
        class="m-b"
      >
        <template slot="content">
          <p>{{ $t(need.description) }}</p>
        </template>
      </AppAccordion>
    </div>
    <div class="flex need__container hide-for-mobile">
      <div class="need__list flex flex-wrap">
        <div
          v-for="need in needList"
          :key="need.id"
          @click="changeNeedDataHandler(need.id)"
        >
          <h5>{{ $t(need.title) }}</h5>
        </div>
      </div>
      <div class="need__description">
        <h2>{{ $t(needObj.title) }}</h2>
        <p>{{ $t(needObj.description) }}</p>
      </div>
    </div>
  </section>
</template>
<script>
import AppSectionHeading from '@/components/UI/AppSectionHeading'
import AppAccordion from '@/components/UI/AppAccordion'
export default {
  name: 'AppYourNeed',
  components: {
    AppSectionHeading,
    AppAccordion,
  },
  data() {
    return {
      needList: [
        {
          title: 'webDevelopment',
          description: 'webDevelopmentDescription',
          id: 1,
        },
        {
          title: 'mobileAppDevelopment',
          description: 'mobileDevelopmentDescription',
          id: 2,
        },
        {
          title: 'incubationAccelaration',
          description: 'incubationAccelarationDescription',
          id: 3,
        },
        {
          title: 'softwareTestingQA',
          description: 'softwareTestingQADescription',
          id: 4,
        },
        {
          title: 'applicationSupport',
          description: 'applicationSupportDescription',
          id: 5,
        },
        {
          title: 'researchDevelopment',
          description: 'researchDevelopmentDescription',
          id: 6,
        },
        {
          title: 'cloudEnterprise',
          description: 'cloudEnterpriseDescription',
          id: 7,
        },
        {
          title: 'devopsService',
          description: 'devopsServiceDescription',
          id: 8,
        },
        {
          title: 'uiUxProductDesign',
          description: 'uiUxProductDesignDescription',
          id: 9,
        },
        {
          title: 'emergencyResponse',
          description: 'emergencyResponseDescription',
          id: 10,
        },
        {
          title: 'dataAnalyticsAIML',
          description: 'dataAnalyticsDescription',
          id: 11,
        },
        {
          title: 'softwareProgramming',
          description: 'softwareProgrammingDescription',
          id: 12,
        },
      ],
      needObj: {},
    }
  },
  mounted() {
    this.changeNeedDataHandler(1)
  },
  methods: {
    changeNeedDataHandler(num) {
      this.needObj = this.needList.find((need) => need.id === num)
    },
  },
}
</script>
<style lang="scss" scoped>
.needSection {
  position: relative;
  &::after {
    content: '';
    position: absolute;
    bottom: -1.5rem;
    background-image: url('@/assets/img/need-arrow.svg');
    background-size: cover;
    background-repeat: no-repeat;
    height: 2.341875rem;
    width: 8.5625rem;
    margin-left: 3rem;
    @include breakpoint-up(large) {
      bottom: -4rem;
      height: 5.613125rem;
      width: 20.52125rem;
      margin-left: 5rem;
    }
  }
}
.need {
  &__list {
    width: 66.666%;
    .active {
      background-color: $gold;
    }
    div {
      background: $dark-grey;
      border: 1px solid $primary-color;
      text-align: center;
      width: 25%;
      padding: 3.125rem 1.875rem;
    }
  }
  &__description {
    width: 33.333%;
    background: $gold;
    border-color: $gold;
    color: $primary-color;
    padding: 3.125rem 2rem;
    h2 {
      margin-bottom: 2rem;
      text-align: center;
    }
    p {
      font-size: 1.2rem;
      line-height: 2.16875rem;
    }
  }
}
</style>
