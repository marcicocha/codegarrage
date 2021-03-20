<template>
  <div>
    <section class="container padding">
      <h6>What we offer</h6>
      <h3>
        Some highlights of our favorite projects we've done for forward thinking
        clients.
      </h3>
      <br />
      <div class="service-img">
        <img src="@/assets/img/idea/driveMe.svg" alt="driveMe" />
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
          title: 'Website Development',
          description:
            'Tap into our deep web development expertise to build any web solution your company feels the need to receive: from single-page websites to complex enterprise-sized web portals and including everything in between.',
          badgeList: ['Front-End Development', 'Back-End Development'],
        },
        {
          title: 'Mobile App Development',
          description:
            'Our Android, iOS, and cross-platform solutions meet all the modern requirements and utilize best practices in terms of functionality, security, scalability and other parameters.',
          badgeList: ['Flutter', 'React-Native'],
        },
        {
          title: 'Cloud Application Development',
          description:
            'Codegarrage ensures you get the best of end-to-end cloud managed services, including cloud infrastructure consulting, troubleshooting, management, monitoring, and security for your cloud applications',
          badgeList: ['DevsecOPs'],
        },
        {
          title: 'Cloud Application Development',
          description:
            'Codegarrage ensures you get the best of end-to-end cloud managed services, including cloud infrastructure consulting, troubleshooting, management, monitoring, and security for your cloud applications',
          badgeList: ['DevsecOPs'],
        },
        {
          title: 'Cloud Application Development',
          description:
            'Codegarrage ensures you get the best of end-to-end cloud managed services, including cloud infrastructure consulting, troubleshooting, management, monitoring, and security for your cloud applications',
          badgeList: ['DevsecOPs'],
        },
        {
          title: 'Cloud Application Development',
          description:
            'Codegarrage ensures you get the best of end-to-end cloud managed services, including cloud infrastructure consulting, troubleshooting, management, monitoring, and security for your cloud applications',
          badgeList: ['DevsecOPs'],
        },
        {
          title: 'Cloud Application Development',
          description:
            'Codegarrage ensures you get the best of end-to-end cloud managed services, including cloud infrastructure consulting, troubleshooting, management, monitoring, and security for your cloud applications',
          badgeList: ['DevsecOPs'],
        },
        {
          title: 'Cloud Application Development',
          description:
            'Codegarrage ensures you get the best of end-to-end cloud managed services, including cloud infrastructure consulting, troubleshooting, management, monitoring, and security for your cloud applications',
          badgeList: ['DevsecOPs'],
        },
        {
          title: 'Cloud Application Development',
          description:
            'Codegarrage ensures you get the best of end-to-end cloud managed services, including cloud infrastructure consulting, troubleshooting, management, monitoring, and security for your cloud applications',
          badgeList: ['DevsecOPs'],
        },
        {
          title: 'Cloud Application Development',
          description:
            'Codegarrage ensures you get the best of end-to-end cloud managed services, including cloud infrastructure consulting, troubleshooting, management, monitoring, and security for your cloud applications',
          badgeList: ['DevsecOPs'],
        },
        {
          title: 'Cloud Application Development',
          description:
            'Codegarrage ensures you get the best of end-to-end cloud managed services, including cloud infrastructure consulting, troubleshooting, management, monitoring, and security for your cloud applications',
          badgeList: ['DevsecOPs'],
        },
        {
          title: 'Cloud Application Development',
          description:
            'Codegarrage ensures you get the best of end-to-end cloud managed services, including cloud infrastructure consulting, troubleshooting, management, monitoring, and security for your cloud applications',
          badgeList: ['DevsecOPs'],
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
