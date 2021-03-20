<template>
  <section class="container padding">
    <AppSectionHeading
      class="needSection"
      title="YOUR NEEDS"
      description="OUR SERVICES"
    />
    <div class="hide-for-desktop">
      <AppAccordion
        v-for="need in needList"
        :key="need.id"
        :heading="need.title"
        :init-is-true="false"
        class="m-b"
      >
        <template slot="content">
          <p>{{ need.description }}</p>
        </template>
      </AppAccordion>
    </div>
    <div class="flex need__container hide-for-mobile">
      <div class="need__list flex flex-wrap">
        <div
          :class="{ active: needObj.id === 1 }"
          @click="changeNeedDataHandler(1)"
        >
          <h3>Web Development</h3>
        </div>
        <div
          :class="{ active: needObj.id === 2 }"
          @click="changeNeedDataHandler(2)"
        >
          <h3>Mobile App Development</h3>
        </div>
        <div
          :class="{ active: needObj.id === 3 }"
          @click="changeNeedDataHandler(3)"
        >
          <h3>Cloud Application Development</h3>
        </div>
        <div
          :class="{ active: needObj.id === 4 }"
          @click="changeNeedDataHandler(4)"
        >
          <h3>Custom Software Development</h3>
        </div>
        <div
          :class="{ active: needObj.id === 5 }"
          @click="changeNeedDataHandler(5)"
        >
          <h3>Application Maintenance &amp; Support</h3>
        </div>
        <div
          :class="{ active: needObj.id === 6 }"
          @click="changeNeedDataHandler(6)"
        >
          <h3>UX &amp; UI Design</h3>
        </div>
        <div
          :class="{ active: needObj.id === 7 }"
          @click="changeNeedDataHandler(7)"
        >
          <h3>DevOps as a Service</h3>
        </div>
        <div
          :class="{ active: needObj.id === 8 }"
          @click="changeNeedDataHandler(8)"
        >
          <h3>Software Product Engineering</h3>
        </div>
        <div
          :class="{ active: needObj.id === 9 }"
          @click="changeNeedDataHandler(9)"
        >
          <h3>Application Maintenance &amp; Support</h3>
        </div>
        <div
          :class="{ active: needObj.id === 10 }"
          @click="changeNeedDataHandler(10)"
        >
          <h3>UX &amp; UI Design</h3>
        </div>
        <div
          :class="{ active: needObj.id === 11 }"
          @click="changeNeedDataHandler(11)"
        >
          <h3>DevOps as a Service</h3>
        </div>
        <div
          :class="{ active: needObj.id === 12 }"
          @click="changeNeedDataHandler(12)"
        >
          <h3>Software Product Engineering</h3>
        </div>
      </div>
      <div class="need__description">
        <h2>{{ needObj.title }}</h2>
        <p>{{ needObj.description }}</p>
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
          title: 'Web Development',
          description:
            'Tap into our deep web development expertise to build any web solution your company feels the need to receive: from single-page websites to complex enterprise-sized web portals and including everything in between.',
          id: 1,
        },
        {
          title: 'Mobile App Development',
          description:
            'Tap into our deep web development expertise to build any web solution your company feels the need to receive: from single-page websites to complex enterprise-sized web portals and including everything in between.',
          id: 2,
        },
        {
          title: 'Cloud Application Development',
          description:
            'Tap into our deep web development expertise to build any web solution your company feels the need to receive: from single-page websites to complex enterprise-sized web portals and including everything in between.',
          id: 3,
        },
        {
          title: 'Custom Software Development',
          description:
            'Tap into our deep web development expertise to build any web solution your company feels the need to receive: from single-page websites to complex enterprise-sized web portals and including everything in between.',
          id: 4,
        },
        {
          title: 'Application Maintenance & Support',
          description:
            'Tap into our deep web development expertise to build any web solution your company feels the need to receive: from single-page websites to complex enterprise-sized web portals and including everything in between.',
          id: 5,
        },
        {
          title: 'UX & UI Design',
          description:
            'Tap into our deep web development expertise to build any web solution your company feels the need to receive: from single-page websites to complex enterprise-sized web portals and including everything in between.',
          id: 6,
        },
        {
          title: 'DevOps as a Service',
          description:
            'Tap into our deep web development expertise to build any web solution your company feels the need to receive: from single-page websites to complex enterprise-sized web portals and including everything in between.',
          id: 7,
        },
        {
          title: 'Software Product Engineering',
          description:
            'Tap into our deep web development expertise to build any web solution your company feels the need to receive: from single-page websites to complex enterprise-sized web portals and including everything in between.',
          id: 8,
        },
        {
          title: 'Application Maintenance & Support',
          description:
            'Tap into our deep web development expertise to build any web solution your company feels the need to receive: from single-page websites to complex enterprise-sized web portals and including everything in between.',
          id: 9,
        },
        {
          title: 'UX & UI Design',
          description:
            'Tap into our deep web development expertise to build any web solution your company feels the need to receive: from single-page websites to complex enterprise-sized web portals and including everything in between.',
          id: 10,
        },
        {
          title: 'DevOps as a Service',
          description:
            'Tap into our deep web development expertise to build any web solution your company feels the need to receive: from single-page websites to complex enterprise-sized web portals and including everything in between.',
          id: 11,
        },
        {
          title: 'Software Product Engineering',
          description:
            'Tap into our deep web development expertise to build any web solution your company feels the need to receive: from single-page websites to complex enterprise-sized web portals and including everything in between.',
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
    padding: 3.125rem 1.875rem;
    h2 {
      margin-bottom: 2rem;
      text-align: center;
    }
    p {
      font-size: 1.5rem;
      line-height: 2.16875rem;
    }
  }
}
</style>
