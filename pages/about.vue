<template>
  <div>
    <section class="container padding">
      <div>
        <h3 class="column-6">
          {{ $t('aboutHeading') }}
        </h3>
      </div>
    </section>
    <section class="container padding">
      <div class="flex flex-ai-c who-container">
        <div class="column-6 about__text">
          <h5>{{ $t('whoWeAre') }}</h5>
          <p>
            {{ $t('whoWeAreDescription') }}
          </p>
        </div>
        <div class="column-6 about__image">
          <div class="about__image-container">
            <div class="about-gold1">
              <span>{{ $t('softwareConsulting') }}</span>
            </div>
            <div class="about-red">
              <span>{{ $t('dataRelated') }}</span>
            </div>
            <div class="about-gold2">
              <span>{{ $t('digitalTransformation') }}</span>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="container padding">
      <div>
        <h6>{{ $t('meetTheTeam') }}</h6>
        <div class="within__container p-tb">
          <h3 class="m-b">{{ $t('within') }}</h3>
          <br />
          <AppCarousel :image-list="withinImgList" />
          <!-- <AppImageSlider :image-list="withinImgList" /> -->
        </div>
        <div class="beyond__container p-tb">
          <h3 class="m-b">{{ $t('beyond') }}</h3>
          <br />
          <AppCarousel :image-list="beyondImgList" />
          <!-- <AppImageSlider :image-list="beyondImgList" /> -->
        </div>
      </div>
    </section>
    <section class="container padding">
      <h2 class="m-b">
        {{ $t('seamlessCollaboration') }}
      </h2>
      <br />
      <div class="flex flex-wrap flex-ai-c">
        <div
          v-for="(about, i) in aboutList"
          :key="i"
          class="info-flex column-6 p-tb"
        >
          <div class="p-r">
            <h2 class="styled__h2">{{ about.id }}</h2>
          </div>
          <div class="p-l">
            <h6>{{ $t(about.title) }}</h6>
            <h5>{{ $t(about.heading) }}</h5>
            <p>
              {{ $t(about.description) }}
            </p>
          </div>
        </div>
      </div>
    </section>
    <section class="container padding">
      <AppYourWords />
    </section>
  </div>
</template>
<script>
import AppYourWords from '@/components/indexPage/AppYourWords'
// import AppImageSlider from '@/components/UI/AppImageSlider'
import AppCarousel from '@/components/about/AppCarousel'
export default {
  components: {
    AppYourWords,
    AppCarousel,
    // AppImageSlider,
  },
  data() {
    return {
      withinImgList: [
        '/within/img1.jpg',
        '/within/img2.jpg',
        '/within/img3.jpg',
      ],
      beyondImgList: [
        '/beyond/img1.jpg',
        '/beyond/img2.jpg',
        '/beyond/img3.jpg',
      ],
      aboutList: [
        {
          id: '01',
          title: 'recieve',
          heading: 'recieveHeading',
          description: 'recieveDescription',
        },
        {
          id: '02',
          title: 'react',
          heading: 'reactHeading',
          description: 'reactDescription',
        },
        {
          id: '03',
          title: 'respond',
          heading: 'respondHeading',
          description: 'respondDescription',
        },
        {
          id: '04',
          title: 'revise',
          heading: 'reviseHeading',
          description: 'reviseDescription',
        },
      ],
    }
  },
}
</script>
<style lang="scss" scoped>
.within__container {
  h3 {
    color: $gold;
  }
}
.beyond-container {
  h3 {
    color: $dark-red;
  }
}
.info-flex {
  display: flex;
  align-items: center;
  justify-content: space-between;
  @include breakpoint-up(large) {
    &:nth-child(odd) {
      padding-right: 1.5rem;
    }
    &:nth-child(even) {
      padding-left: 1.5rem;
    }
  }
}

.who-container {
  .about {
    &__text {
      order: 2;
      margin-bottom: 2rem;
    }
    &__image {
      order: 1;
      &-container {
        display: flex;
        // justify-content: center;
        div {
          position: relative;
          width: 4.5625rem;
          height: 21.75rem;
          margin: 1.5rem;
          border-radius: 0.25rem;
          font-size: $s16;
          font-family: $nunito;
          font-weight: 900;
          &::after {
            content: '';
            position: absolute;
            width: 100%;
            height: 100%;
            border: 1px solid #443323;
            transition: top 2s, left 4s, opacity 4s;
          }
          @include breakpoint-up(large) {
            width: 5.875rem;
            height: 27.8125rem;
            font-size: 1.375rem;
          }
          &:not(:nth-child(2)) {
            background: $gold;
            top: 5rem;
          }
          &:first-child {
            top: 2.5rem;
            animation: fadeInDown 1s;
            &::after {
              top: -2rem;
              left: 1.2rem;
              animation: fadeInTopLeft 2s;
            }
          }
          &:nth-child(2) {
            background: $dark-red;
            animation: fadeInDown 2s;
            animation-timing-function: linear;
            &::after {
              height: 90%;
              top: 2rem;
              left: 1.2rem;
              animation: slideInUp 3s;
            }
          }
          &:last-child {
            top: 2.5rem;
            animation: fadeInDown 2s;
            &::after {
              height: 90%;
              top: 1.5rem;
              left: 1.2rem;
              animation: fadeInTopRight 2s;
            }
          }
          span {
            position: absolute;
            top: 7rem;
            left: -9.5rem;
            // transform-origin: center;
            transform: rotate(-90deg);
            z-index: 2;
            width: 23.5rem;
            @include breakpoint-up(large) {
              top: 12rem;
              left: -9rem;
              width: 25rem;
            }
          }
        }
      }
    }
  }
}
.styled__h2 {
  position: relative;
  font-weight: 900;
  background: $gold;
  padding-left: 0.25rem;
  padding-right: 0.25rem;
  border-radius: 0.25rem;
  margin-left: 0.5rem;
  font-size: 1.25rem;
  @include breakpoint-up(large) {
    margin-left: 1rem;
    padding-left: 0.5rem;
    padding-right: 0.5rem;
    font-size: 1.5rem;
  }
  &::after {
    content: '';
    position: absolute;
    top: -0.5rem;
    left: -0.5rem;
    width: 100%;
    height: 100%;
    background-color: $dark-red;
    border-radius: 0.25rem;
    z-index: -1;
    @include breakpoint-up(large) {
      top: -0.8rem;
      left: -0.8rem;
    }
  }
}
</style>
