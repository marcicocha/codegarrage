<template>
  <div>
    <section class="container padding">
      <h6>OUR WORK</h6>
      <h3>
        At Codegarrage, you will be a member of our talented team which has been
        bringing business ideas to life. Our mission is to create solutions that
        improve the lives of people in a convenient and secure way. The creation
        of such solutions requires the involvement of committed people and new
        innovative approaches they bring along. That is why we are looking for
        talented professionals to join our team.
      </h3>
      <br />
      <button class="button">SEE JOB OPENINGS</button>
    </section>
    <section class="container padding">
      <h2 class="benefit-heading p-tb">Benefits</h2>

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
          title: 'Smart, kind colleagues',
          description:
            'Learn and grow with highly accomplished colleagues who’re invested in your personal and professional development.',
        },
        {
          id: '02',
          title: 'Housing assistance',
          description:
            'We offer subsidized housing and relocation grants to all team members',
        },
        {
          id: '03',
          title: 'Smart, kind colleagues',
          description:
            'Learn and grow with highly accomplished colleagues who’re invested in your personal and professional development.',
        },
        {
          id: '04',
          title: 'Training programs',
          description:
            'We invest in our people to ensure they can achieve their short, medium, and long term professional goals',
        },
        {
          id: '05',
          title: 'Competitive salary',
          description:
            'Our renumeration packages are in line with industry standards, commiserate to job roles, and functions and performance driven',
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
