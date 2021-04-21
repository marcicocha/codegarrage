<template>
  <section class="container padding">
    <AppSectionHeading
      class="companySection"
      title="OUR COMPANY"
      description="OUR CULTURE"
    />

    <div class="flex flex-jc-sb work">
      <div class="column-6 m-b">
        <h6>WORK</h6>
        <p>
          We take pride in our outstanding client care services being known as
          one of the top quality care support specialists globally. With a mix
          of our technical expertise, and experience, we provide nothing else
          but excellence.
        </p>
        <p>
          The success of our company is dependent on our ability to anticipate
          clients needs, adapt software solutions to these needs and provide
          corporations with vital planning tools.
        </p>
      </div>
      <div class="column-6">
        <img src="@/assets/img/within/img2.jpg" alt="work-image" />
      </div>
    </div>
    <div class="flex flex-jc-sb leisure">
      <div class="column-6 m-b">
        <h6>LEISURE</h6>
        <p>
          We value our employees commitment and their timely response to client
          claims, by offering top notch tech service delivery.
        </p>
        <p>
          An all inclusive employer we seek work life balance for our employees
          and provide opportunities for team bonding, relaxation and fun.
        </p>
      </div>
      <div class="column-6">
        <img src="@/assets/img/beyond/img3.jpg" alt="leisure-image" />
      </div>
    </div>
    <div class="padding expertise">
      <div style="margin-bottom: 2rem">
        <h6>EXPERTISE</h6>
        <p>Powering growth for amazing businesses</p>
      </div>
      <div class="logos">
        <div><img src="@/assets/img/company-logo/ios.svg" alt="ios" /></div>
        <div>
          <img
            src="@/assets/img/company-logo/green-hexagon.svg"
            alt="green-hexagon"
          />
        </div>
        <div>
          <img src="@/assets/img/company-logo/andriod.svg" alt="andriod" />
        </div>
        <div><img src="@/assets/img/company-logo/php.svg" alt="php" /></div>
        <div><img src="@/assets/img/company-logo/react.svg" alt="react" /></div>
        <div><img src="@/assets/img/company-logo/ruby.svg" alt="ruby" /></div>
        <div>
          <img src="@/assets/img/company-logo/phython.svg" alt="phython" />
        </div>
        <div>
          <img src="@/assets/img/company-logo/angular.svg" alt="angular" />
        </div>
        <div><img src="@/assets/img/company-logo/java.svg" alt="java" /></div>
        <div>
          <img
            src="@/assets/img/company-logo/javascript.svg"
            alt="javascript"
          />
        </div>
        <div>
          <img
            src="@/assets/img/company-logo/microsoft-azure.svg"
            alt="microsoft-azure"
          />
        </div>
        <div>
          <img src="@/assets/img/company-logo/google.svg" alt="google" />
        </div>
        <div>
          <img src="@/assets/img/company-logo/tableau.svg" alt="tableau" />
        </div>
        <div>
          <img
            src="@/assets/img/company-logo/apache-spark.svg"
            alt="apache-spark"
          />
        </div>
        <div>
          <img src="@/assets/img/company-logo/hadoop.svg" alt="hadoop" />
        </div>
        <div><img src="@/assets/img/company-logo/aws.svg" alt="aws" /></div>
        <div><img src="@/assets/img/company-logo/figma.svg" alt="figma" /></div>
        <div><img src="@/assets/img/company-logo/vue.svg" alt="vue" /></div>
        <div>
          <img src="@/assets/img/company-logo/flutter.svg" alt="flutter" />
        </div>
        <div>
          <img
            src="@/assets/img/company-logo/adobe-illustrator.svg"
            alt="adobe-illustrator"
          />
        </div>
        <div>
          <img
            src="@/assets/img/company-logo/typescript.svg"
            alt="typescript"
          />
        </div>
        <div><img src="@/assets/img/company-logo/jest.svg" alt="jest" /></div>
        <div>
          <img
            src="@/assets/img/company-logo/google-cloud.svg"
            alt="google-cloud"
          />
        </div>
      </div>
    </div>
  </section>
</template>
<script>
import AppSectionHeading from '@/components/UI/AppSectionHeading'

export default {
  name: 'AppOurCompany',
  components: {
    AppSectionHeading,
  },
}
</script>
<style lang="scss" scoped>
.companySection {
  position: relative;
  &::after {
    content: '';
    position: absolute;
    bottom: -1rem;
    background-image: url('@/assets/img/company-arrow.svg');
    background-size: contain;
    height: 1.4875rem;
    width: 10.25rem;
    margin-left: 4rem;
    @include breakpoint-up(large) {
      bottom: -2rem;
      height: 3.709375rem;
      width: 24.03125rem;
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
      &:nth-child(15),
      &:nth-child(23) {
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
          left: 0;
        }
        &:nth-child(14) {
          width: 14.2857%;
          img {
            width: 60%;
          }
        }
        &:first-child,
        &:nth-child(8),
        &:nth-child(14) {
          text-align: left;
        }
        &:nth-child(7),
        &:nth-child(13) {
          text-align: right;
          img {
            right: 0;
          }
        }
        &:nth-child(13),
        &:nth-child(15),
        &:nth-child(23) {
          width: 24%;
          img {
            width: 75%;
            object-position: center;
          }
        }
        &:nth-child(16) {
          img {
            width: 50%;
            object-position: center;
          }
        }
        &:nth-child(17),
        &:nth-child(19) {
          img {
            width: 25%;
            object-position: center;
          }
        }
      }
    }
  }
}
</style>
