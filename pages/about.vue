<template>
  <div>
    <section class="container padding">
      <div>
        <h3 class="column-6">
          A software development company that uses strategy, branding and
          technology to help reach business and user objectives.
        </h3>
      </div>
    </section>
    <section class="container padding">
      <div class="flex flex-ai-c who-container">
        <div class="column-6 about__text">
          <h5>WHO WE ARE</h5>
          <p>
            We’re a team of makers, thinkers and explorers. We design and build
            digital products because we’re curious people driven by continious
            learning and solving hard problems. We gain a huge amount of
            fulfilment through growing our clients businesses, delighting their
            customers, and innovating in their industries.
          </p>
        </div>
        <div class="column-6 about__image">
          <div class="about__image-container">
            <div class="about-gold1"><span>Software Consulting</span></div>
            <div class="about-red">
              <span>Data-Related Software Engineering</span>
            </div>
            <div class="about-gold2"><span>Digital Transformation</span></div>
          </div>
        </div>
      </div>
    </section>
    <section class="container padding">
      <div>
        <h6>MEET THE TEAM</h6>
        <div class="within__container p-tb">
          <h3 class="m-b">WITHIN THE OFFICE WALLS</h3>
          <br />
          <AppCarousel :image-list="withinImgList" />
          <!-- <AppImageSlider :image-list="withinImgList" /> -->
        </div>
        <div class="beyond__container p-tb">
          <h3 class="m-b">BEYOND THE OFFICE WALLS</h3>
          <br />
          <AppCarousel :image-list="beyondImgList" />
          <!-- <AppImageSlider :image-list="beyondImgList" /> -->
        </div>
      </div>
    </section>
    <section class="container padding">
      <h2 class="m-b">
        Seamless collaboration, total transparency, secure delivery.
      </h2>
      <br />
      <div class="flex flex-wrap flex-ai-c">
        <div class="info-flex column-6 p-tb">
          <div class="p-r">
            <h2 class="styled__h2">01</h2>
          </div>
          <div class="p-l">
            <h6>RECEIVE</h6>
            <h5>Understand your business &amp; Users</h5>
            <p>
              We work with you to define business goals, identify feasible
              technologies, define timelines and help you achieve success.
            </p>
          </div>
        </div>
        <div class="info-flex column-6 p-tb">
          <div class="p-r"><h2 class="styled__h2">02</h2></div>
          <div class="p-l">
            <h6>REACT</h6>
            <h5>Plan product strategy</h5>
            <p>
              We'll work with you and other key stakeholders to prioritise
              objectives and formulate a proven strategy.
            </p>
          </div>
        </div>
        <div class="info-flex column-6 p-tb">
          <div class="p-r"><h2 class="styled__h2">03</h2></div>
          <div class="p-l">
            <h6>RESPOND</h6>
            <h5>Research, ideate &amp; design</h5>
            <p>
              We turn qualitative and quantiative data into world-class, user
              friendly experiences that your customers love
            </p>
          </div>
        </div>
        <div class="info-flex column-6 p-tb">
          <div class="p-r"><h2 class="styled__h2">04</h2></div>
          <div class="p-l">
            <h6>REVISE</h6>
            <h5>Execute, track &amp; iterate</h5>
            <p>
              Once your product is live, we will help with tracking the
              performance and provide rapid iterations to constantly improve
              it's results.
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
import AppCarousel from '@/components/UI/AppCarousel'
export default {
  components: {
    AppYourWords,
    AppCarousel,
    // AppImageSlider,
  },
  data() {
    return {
      withinImgList: [
        '/within/img1.svg',
        '/within/img2.svg',
        '/within/img3.svg',
      ],
      beyondImgList: [
        '/beyond/img1.svg',
        '/beyond/img2.svg',
        '/beyond/img3.svg',
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
            &::after {
              top: -2rem;
              left: 1.2rem;
            }
          }
          &:nth-child(2) {
            background: $dark-red;
            &::after {
              height: 90%;
              top: 2rem;
              left: 1.2rem;
            }
          }
          &:last-child {
            top: 2.5rem;
            &::after {
              height: 90%;
              top: 1.5rem;
              left: 1.2rem;
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
