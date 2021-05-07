<template>
  <section class="container flex flex-jc-sb">
    <div class="column-6 p-right intro__heading" style="margin-bottom: 3rem">
      <h2>
        {{ $t('introTitle') }}
      </h2>
      <br />
      <p>
        {{ $t('introDescription') }}
      </p>
    </div>
    <div class="column-6" style="margin-bottom: 4rem">
      <div class="intro__image">
        <div class="intro__image-container">
          <div class="div__title title1"><h1>01</h1></div>
          <div class="div__text text1">
            <span>{{ $t('dataRelated') }}</span>
          </div>
        </div>
        <div class="intro__image-container">
          <div class="div__title title2"><h1>02</h1></div>
          <div class="div__text text2">
            <span>{{ $t('softwareConsulting') }}</span>
          </div>
        </div>
        <div class="intro__image-container">
          <div class="div__title title3"><h1>03</h1></div>
          <div class="div__text text3">
            <span>{{ $t('digitalTransformation') }}</span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  name: 'AppIntroPage',
}
</script>
<style lang="scss" scoped>
.p-right {
  @include breakpoint-up(large) {
    margin-top: 3rem;
    padding-right: 2rem;
  }
}
.intro {
  &__heading {
    animation: slideInLeft 2s;
  }
  &__image {
    display: flex;
    justify-content: center;
    // min-height: 400px;
    &-container {
      position: relative;
      margin: 0.5rem;
      @include breakpoint-up(large) {
        margin: 1rem;
      }
      .div {
        &__title {
          position: relative;
          background: $gold;
          width: 3rem;
          padding: 0.5rem;
          text-align: right;
          margin: 0;
          @include breakpoint-up(large) {
            width: 5rem;
          }
          &::after {
            content: '';
            position: absolute;
            border: 1px solid #443323;
            width: 100%;
            height: 100%;
          }
        }
        &__text {
          position: absolute;
          background: $dark-red;
          height: 2.75rem;
          padding: 0.5rem;
          margin: 0;
          z-index: 2;
          span {
            position: absolute;
            top: 20%;
            bottom: 0;
            left: 5px;
            font-family: $nunito;
            font-size: 0.75rem;
            font-weight: 800;
            line-height: 1rem;
          }
          @include breakpoint-up(large) {
            height: 5.5625rem;
            span {
              top: 25%;
              font-weight: 800;
              font-size: 1.25rem;
              line-height: 1.5rem;
              left: 10px;
            }
          }
        }
      }
      .title1 {
        height: 6.674375rem;
        animation: fadeInDown 2s;
        @include breakpoint-up(large) {
          height: 13.08875rem;
        }
        &::after {
          left: 20%;
          top: 6%;
          animation: fadeInRight 2s;
        }
      }
      .title2 {
        animation: fadeInDown 1s;
        &::after {
          top: -10%;
          left: 20%;
          animation: fadeInLeft 2s;
        }
      }
      .title3 {
        animation: fadeInDown 1s;
        &::after {
          left: 80%;
          animation: fadeInRight 2s;
        }
        h1 {
          position: absolute;
          bottom: 40%;
        }
      }
      .title1,
      .title3 {
        top: 4rem;

        @include breakpoint-up(large) {
          top: 6rem;
        }
      }
      .title2,
      .title3 {
        height: 11.5rem;
        @include breakpoint-up(large) {
          height: 23.125rem;
        }
      }
      .text1 {
        top: 60%;
        right: -20%;
        width: 9rem;
        animation: slideInRight 3s;
        @include breakpoint-up(large) {
          top: 49%;
          right: -35%;
          width: 16rem;
        }
      }
      .text2 {
        top: 25%;
        left: 55%;
        animation: slideInRight 3s;
      }
      .text3 {
        bottom: -25%;
        left: -55%;
        animation: slideInRight 3s;
        @include breakpoint-up(large) {
          bottom: -20%;
        }
      }
      .text2,
      .text3 {
        width: 9.4375rem;
        @include breakpoint-up(large) {
          width: 17rem;
        }
      }
    }
  }
}
</style>
