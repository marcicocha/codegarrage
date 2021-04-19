<template>
  <div>
    <AppIntroPage />
    <AppOurCompany />
    <AppYourNeed />
    <section class="container padding">
      <AppSectionHeading
        class="ideaSection"
        title="YOUR IDEAS"
        description="OUR PORTFOLIO"
      />
      <AppYourIdeas isHomePage />
    </section>

    <AppOurLeaders />

    <section class="container padding">
      <AppSectionHeading
        class="wordSection"
        title="YOUR WORDS"
        description="OUR MOTIVATION"
      />
      <br />
      <AppYourWords />
    </section>
  </div>
</template>
<script>
import AppIntroPage from '@/components/indexPage/AppIntroPage'
import AppOurCompany from '@/components/indexPage/AppOurCompany'
import AppYourNeed from '@/components/indexPage/AppYourNeed'
import AppYourIdeas from '@/components/indexPage/AppYourIdeas'
import AppYourWords from '@/components/indexPage/AppYourWords'
import AppSectionHeading from '@/components/UI/AppSectionHeading'
import AppOurLeaders from '@/components/indexPage/AppOurLeaders'
export default {
  components: {
    AppIntroPage,
    AppOurCompany,
    AppYourNeed,
    AppYourIdeas,
    AppYourWords,
    AppSectionHeading,
    AppOurLeaders,
  },
}
</script>
<style lang="scss" scoped>
.ideaSection {
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
.wordSection {
  position: relative;
  &::after {
    content: '';
    position: absolute;
    bottom: -1.5rem;
    background-image: url('@/assets/img/word-arrow.svg');
    background-size: cover;
    background-repeat: no-repeat;
    height: 1.850625rem;
    width: 12.75rem;
    margin-left: 1rem;
    @include breakpoint-up(large) {
      bottom: -4rem;
      height: 3.709375rem;
      width: 25.55875rem;
      margin-left: 2rem;
    }
  }
}
</style>
