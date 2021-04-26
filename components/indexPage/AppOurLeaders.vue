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
          imgPath: 'leader/oluwafemi_korede.jpg',
          name: 'Oluwafemi Korede',
          description: 'engineering',
        },
        {
          imgPath: 'leader/sylvia_onwukwe.jpg',
          name: 'Sylvia Onwukwe',
          description: 'engineering',
        },
        {
          imgPath: 'leader/bimpe_ayoola.jpg',
          name: 'Bimpe Ayoola',
          description: 'operationProject',
        },
        {
          imgPath: 'leader/peter_onu.jpg',
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
.expertise {
  .logos {
    display: flex;
    flex-wrap: wrap;
    // justify-content: space-between;
    align-content: center;
    div {
      width: 20%;
      padding: 1rem;
      display: block;
      position: relative;
      &:nth-child(13) {
        width: 60%;
      }
      &:nth-child(14) {
        width: 25%;
      }
      &:nth-child(15) {
        width: 40%;
      }
      img {
        width: 100%;
      }
      @include breakpoint-up(large) {
        width: 14.2857%;
        // text-align: center;
        position: relative;
        height: 6.16rem;
        img {
          width: 30%;
          object-position: center;
          position: absolute;
          top: 0;
        }
        &:first-child,
        &:nth-child(8),
        &:nth-child(14) {
          text-align: left;
        }
        // &:nth-child(7),
        // &:nth-child(13) {
        //   text-align: right;
        // }
        &:nth-child(13),
        &:nth-child(15) {
          width: 28.5714%;
          img {
            width: 50%;
            object-position: center;
          }
        }
      }
    }
  }
}
</style>
