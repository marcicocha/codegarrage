<template>
  <section class="container padding">
    <AppSectionHeading
      class="needSection"
      title="YOUR NEEDS"
      description="OUR SERVICES"
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
          <p>{{ need.description }}</p>
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
          <h5>{{ need.title }}</h5>
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
            'Tap into our deep web development expertise to build any web solution that your company needs, from  dynamic websites to complex enterprise-sized web solutions.',
          id: 1,
        },
        {
          title: 'Mobile App Development',
          description:
            'Steering clients  through digital transformation, we build intuitive and engaging  Android, iOS, and cross-platform for businesses that your end users can adapt to quickly.',
          id: 2,
        },
        {
          title: 'Incubation and Acceleration',
          description:
            'With exclusive access to resources, tools, and services, we support your startup business and help you grow your network of mentors, investors and founders.',
          id: 3,
        },
        {
          title: 'Software Testing/Quality Assurance',
          description:
            'With our unparalleled technical expertise, we implement quality testing frameworks and automation expertise using current testing trends.',
          id: 4,
        },
        {
          title: 'Application Maintenance & Support',
          description:
            'Keeping your application online, secure, updated and bug-free is our main goal, while we deal and resolve real time problems your  application might encounter on a day-to-day operational level.',
          id: 5,
        },
        {
          title: 'Research and Development',
          description:
            'We perform original investigations and research findings to strengthen your software engineering, technical implementation or research thesis, which can be used to create improved technologies. We have talents, labs, processes and infrastructures to deliver world class results to you.',
          id: 6,
        },
        {
          title: 'Cloud and Enterprise application development',
          description:
            'We develop bespoke and streamlined enterprise solutions to automate your internal processes, drive business efficiency and flexibility, and provide advanced insights into your business operations and employees.',
          id: 7,
        },
        {
          title: 'DevOps as a Service',
          description:
            'We offer cloud and devops solutions aimed at high performance, scalability, and agility at a reduced cost to maximize ROI, software availability,  cloud security, and continuous integrations allowing you to  run your solutions as fast as you run your business.',
          id: 8,
        },
        {
          title: 'UI/UX and product design',
          description:
            'We are a design first development company. Projects are driven by designers and they make sure design and experiences translate to code. With expressive design, we give life to brands and create a synergy between the brand and the user.',
          id: 9,
        },
        {
          title: 'Emergency and Response',
          description:
            'This is a key service offered to businesses in need of quick  response to their business or application needs. Our dedicated emergency and response team are always available on a 24/7 hour basis to streamline your processes and give life to dying businesses or solutions.',
          id: 10,
        },
        {
          title: 'Data Analytics/AI/ML',
          description:
            'With our decades of expertise in the areas of Artificial intelligence, deep learning, machine learning, and data analysis; we build highly intelligent, automated, and analytical solutions for businesses to fast-track your problem-solving capabilities.',
          id: 11,
        },
        {
          title: 'Software Programming Mentorship and consulting',
          description:
            ' Business goals, technical requirements, project scoping and programing mentorship as we push the edge of innovations with our technical competencies and our delivery track record.',
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
