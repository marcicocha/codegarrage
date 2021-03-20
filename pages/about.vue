<template>
  <div>
    <section class="container padding">
      <div>
        <h2>
          A software development company that uses strategy, branding and
          technology to help reach business and user objectives.
        </h2>
      </div>
    </section>
    <section class="container padding">
      <div class="flex flex-ai-c who-container">
        <div class="column-6">
          <h5>WHO WE ARE</h5>
          <p>
            We’re a team of makers, thinkers and explorers. We design and build
            digital products because we’re curious people driven by continious
            learning and solving hard problems. We gain a huge amount of
            fulfilment through growing our clients businesses, delighting their
            customers, and innovating in their industries.
          </p>
        </div>
        <div class="column-6"></div>
      </div>
    </section>
    <section class="container padding">
      <div>
        <h6>MEET THE TEAM</h6>
        <div class="within__container p-tb">
          <h3 class="m-b">WITHIN THE OFFICE WALLS</h3>
          <AppImageSlider :image-list="withinImgList" />
        </div>
        <div class="beyond__container p-tb">
          <h3 class="m-b">BEYOND THE OFFICE WALLS</h3>
          <AppImageSlider :image-list="beyondImgList" />
        </div>
      </div>
    </section>
    <section class="container padding">
      <h2>Seamless collaboration, total transparency, secure delivery.</h2>
      <div class="flex flex-wrap flex-ai-c">
        <div class="info-flex column-6 p-tb">
          <div class="p-r">
            <h2 class="styled__h2">01</h2>
          </div>
          <div class="p-l">
            <h6>RECEIVE</h6>
            <h3>Understand your business &amp; Users</h3>
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
            <h3>Plan product strategy</h3>
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
            <h3>Research, ideate &amp; design</h3>
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
            <h3>Execute, track &amp; iterate</h3>
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
import AppImageSlider from '@/components/UI/AppImageSlider'
export default {
  components: {
    AppYourWords,
    AppImageSlider,
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
}
.who-container {
  div {
    &:first-child {
      order: 2;
    }
    &:last-child {
      order: 1;
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
    font-size: 2rem;
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
