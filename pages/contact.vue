<template>
  <div>
    <section class="container padding">
      <h6>Contact Us</h6>
      <h3 class="column-6">
        Feel free to contact us at any time that you find convenient, You will
        receive a response in the shortest time possible.
      </h3>
    </section>
    <section class="container padding">
      <div class="flex flex-jc-sb flex-ai-c">
        <div class="column-6 contact__image">
          <div>
            <img src="@/assets/img/contact-us.JPG" />
          </div>
        </div>
        <div class="column-6 contact__field">
          <div class="flex flex-jc-sb input-container">
            <AppInput
              v-model="contactObject.firstName"
              placeholder="First Name"
              icon-path="user.svg"
              class="margin-right"
            />
            <AppInput
              v-model="contactObject.lastName"
              placeholder="Last Name"
              icon-path="user.svg"
              class="margin-left"
            />
          </div>
          <div class="flex flex-jc-sb input-container">
            <AppInput
              v-model="contactObject.email"
              placeholder="Email"
              icon-path="email.svg"
              class="margin-right"
            />
            <AppInput
              v-model="contactObject.companyName"
              placeholder="Company Name"
              icon-path="home.svg"
              class="margin-left"
            />
          </div>
          <AppInput
            v-model="contactObject.phoneNumber"
            placeholder="Phone Number"
            type="phone"
            icon-path="phone.svg"
          />
          <AppTextArea
            v-model="contactObject.message"
            placeholder="Message"
            icon-path="edit.svg"
          />
          <br />
          <button class="button">SEND MESSAGE</button>
        </div>
      </div>
    </section>
    <section class="container padding">
      <h2 class="benefit-heading p-tb m-b">Office locations</h2>
      <br />
      <div class="flex flex-jc-c card-parent">
        <AppCard
          v-for="(office, i) in officeList"
          :key="i"
          :card-obj="office"
          class="card"
        />
      </div>
    </section>
  </div>
</template>
<script>
import AppCard from '@/components/UI/AppCard'
import AppInput from '@/components/UI/AppInput'
import AppTextArea from '@/components/UI/AppTextArea'
export default {
  components: {
    AppCard,
    AppInput,
    AppTextArea,
  },
  data() {
    return {
      contactObject: {},
      officeList: [
        {
          title: 'Lagos Office',
          description: '10, Karimu Ikotun close, Sabo Lagos, Nigeria.',
          imgPath: 'office-location/lagos-office.svg',
        },
        {
          title: 'Ibadan Office',
          description:
            'CodeGarage Building, Omolayo Bus-Stop, Akobo, Ibadan, Nigeria.',
          imgPath: 'office-location/ibadan-office.svg',
        },
      ],
    }
  },
}
</script>
<style lang="scss" scoped>
.contact {
  &__image {
    order: 2;
    margin-bottom: 2rem;
    width: 100%;
    img {
      width: 100%;
    }
    @include breakpoint-up(large) {
      width: 50%;
      margin-left: 1rem;
    }
  }
  &__field {
    order: 1;
    @include breakpoint-up(large) {
      margin-right: 1rem;
    }
  }
}
.benefit-heading {
  position: relative;
  color: $gold;
  &::after {
    content: '';
    position: absolute;
    bottom: -0.6rem;
    left: 0;
    background-image: url('@/assets/img/need-arrow.svg');
    background-size: cover;
    background-repeat: no-repeat;
    height: 2.878125rem;
    width: 10.07125rem;
    @include breakpoint-up(large) {
      bottom: -1rem;
      height: 3.448125rem;
      width: 12.9375rem;
    }
  }
}
.card {
  @include breakpoint-up(large) {
    width: 25%;
    &:first-child {
      margin-right: 1rem;
    }
    &:last-child {
      margin-left: 1rem;
    }
  }
}
.input-container {
  @include breakpoint-up(large) {
    .margin-right {
      margin-right: 0.5rem;
    }
    .margin-left {
      margin-left: 0.5rem;
    }
  }
}
</style>
