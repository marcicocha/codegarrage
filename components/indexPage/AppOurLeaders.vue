<template>
  <section class="container padding">
    <AppSectionHeading
      class="companySection"
      title="ourCompany"
      description="ourLeaders"
    />
    <br />
    <AppCarousel :image-list="imageList" />
  </section>
</template>
<script>
import AppSectionHeading from '@/components/UI/AppSectionHeading'
import AppCarousel from '@/components/indexPage/AppCarousel'
export default {
  name: 'AppOurLeaders',
  components: {
    AppSectionHeading,
    AppCarousel,
  },
  data() {
    return {
      imageList: [
        {
          imgPath: 'leader/oluwafemi-korede.jpg',
          name: 'Oluwafemi Korede',
          description: 'engineering',
        },
        {
          imgPath: 'leader/sylvia-onwukwe.jpg',
          name: 'Sylvia Onwukwe',
          description: 'engineering',
        },
        {
          imgPath: 'leader/bimpe-ayoola.jpg',
          name: 'Bimpe Ayoola',
          description: 'operationProject',
        },
        {
          imgPath: 'leader/peter-onu.jpg',
          name: 'Peter Onu',
          description: 'businessProject',
        },
      ],
    }
  },
}
</script>
<style lang="scss" scoped>
.companySection {
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
img {
  width: 100%;
}

.work {
  padding-top: 1rem;
  padding-bottom: 1rem;
  @include breakpoint-up(large) {
    padding-top: 3.25rem;
    padding-bottom: 3.25rem;
    div {
      &:first-child {
        margin-right: 4rem;
      }
      &:last-child {
        margin-left: 4rem;
      }
    }
  }
}
.leisure {
  padding-top: 1rem;
  padding-bottom: 1rem;
  @include breakpoint-up(large) {
    padding-top: 3.25rem;
    padding-bottom: 3.25rem;
    div {
      &:first-child {
        order: 2;
        margin-left: 2.5rem;
      }
      &:last-child {
        order: 1;
        margin-right: 2.5rem;
      }
    }
  }
}
</style>
