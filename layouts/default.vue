<template>
  <div>
    <header
      :class="{
        header: true,
        open: overlayIsVisible,
      }"
    >
      <div
        :class="{
          overlay: true,
          'fade-in': overlayIsVisible,
          'fade-out': !overlayIsVisible,
        }"
      ></div>
      <nav class="flex flex-jc-sb flex-ai-c">
        <nuxt-link to="/" class="header__logo"
          ><img src="@/assets/img/logo.svg" alt="logo"
        /></nuxt-link>

        <div
          id="btnHamburger"
          class="header__toggle hide-for-desktop"
          @click="showOverlay"
        >
          <span></span>
          <span></span>
          <span></span>
        </div>

        <div class="header__links hide-for-mobile">
          <nuxt-link to="about"
            ><span>{{ $t('about') }}</span></nuxt-link
          >
          <nuxt-link to="services"
            ><span>{{ $t('services') }}</span></nuxt-link
          >
          <nuxt-link to="portfolio"
            ><span>{{ $t('portfolio') }}</span></nuxt-link
          >
        </div>
        <div class="hide-for-mobile">
          <div class="flex flex-jc-sb flex-ai-c">
            <nuxt-link to="contact" class="button header__button">{{
              $t('contact-us')
            }}</nuxt-link>
            <div class="select_container">
              <div class="flex flex-jc-sb flex-ai-c">
                <p class="languageSelected">
                  {{ language === 'en' ? 'EN' : 'FR' }}
                </p>
                <span class="arrow-down" @click="showSelectField"
                  ><img src="@/assets/img/icon/arrow-down.svg" alt="arrow-down"
                /></span>
              </div>

              <div v-if="visible" class="select d-n">
                <div>
                  <button class="desktop_lang_link" @click="changeLng('fr')">
                    French
                  </button>
                  <button class="desktop_lang_link" @click="changeLng('en')">
                    English
                  </button>
                </div>
              </div>
            </div>
          </div>
        </div>
      </nav>
      <div
        :class="{
          header__menu: true,
          'fade-in': overlayIsVisible,
          'fade-out': !overlayIsVisible,
        }"
      >
        <div @click="showOverlay">
          <nuxt-link to="about"
            ><span>{{ $t('about') }}</span></nuxt-link
          >
        </div>
        <div @click="showOverlay">
          <nuxt-link to="services"
            ><span>{{ $t('services') }}</span></nuxt-link
          >
        </div>
        <div @click="showOverlay">
          <nuxt-link to="portfolio"
            ><span>{{ $t('portfolio') }}</span></nuxt-link
          >
        </div>
        <div @click="showOverlay">
          <nuxt-link to="contact">{{ $t('contact-us') }}</nuxt-link>
        </div>
        <div v-if="language === 'en'" @click="showOverlay">
          <button class="button header__button" @click="changeLng('fr')">
            French
          </button>
        </div>
        <div v-if="language === 'fr'" @click="showOverlay">
          <button class="button header__button" @click="changeLng('en')">
            English
          </button>
        </div>
      </div>
    </header>
    <div ref="scroll" class="child-body">
      <div>
        <Nuxt />
      </div>

      <footer class="footer">
        <section class="container flex flex-jc-sb flex-ai-c">
          <h2>
            {{ $t('footer-description') }}
          </h2>
          <div>
            <nuxt-link to="contact" class="button">{{
              $t('contact-us')
            }}</nuxt-link>
          </div>
        </section>
        <section class="container">
          <div class="border flex">
            <div class="footer__logo">
              <img src="@/assets/img/logo.svg" alt="logo-white" />
              <p>CodegarageAfrica</p>
            </div>
            <div class="footer__details">
              <div class="footer__details_lists flex">
                <div>
                  <p>{{ $t('explore') }}</p>
                  <ul>
                    <li>
                      <nuxt-link to="about"
                        ><span>{{ $t('about') }}</span></nuxt-link
                      >
                    </li>
                    <li>
                      <nuxt-link to="services"
                        ><span>{{ $t('services') }}</span></nuxt-link
                      >
                    </li>
                    <li>
                      <nuxt-link to="portfolio"
                        ><span>{{ $t('portfolio') }}</span></nuxt-link
                      >
                    </li>
                    <li>
                      <nuxt-link to="career"
                        ><span>{{ $t('careers') }}</span></nuxt-link
                      >
                    </li>
                    <!-- <li>
                      <nuxt-link to="/"
                        ><span>{{ $t('testimonial') }}</span></nuxt-link
                      >
                    </li> -->
                  </ul>
                </div>
                <div>
                  <p>{{ $t('contact') }}</p>
                  <ul>
                    <li>services@codegarage.africa</li>
                    <li>08185956620</li>
                  </ul>
                </div>
                <div>
                  <p>{{ $t('follow') }}</p>
                  <ul>
                    <li>
                      <a href="https://twitter.com/CodegarageA" target="_blank"
                        >Twitter</a
                      >
                    </li>
                    <li>
                      <a
                        href="https://www.instagram.com/codegarageafrica/"
                        target="_blank"
                        >Instagram</a
                      >
                    </li>
                    <li>
                      <a
                        href="https://www.linkedin.com/company/codegarage-africa/"
                        target="_blank"
                        >LinkedIn</a
                      >
                    </li>
                  </ul>
                </div>
                <div>
                  <p>{{ $t('legal') }}</p>
                  <ul>
                    <li>{{ $t('terms') }}</li>
                    <li>{{ $t('privacy') }}</li>
                  </ul>
                </div>
                <div>
                  <p>{{ $t('lagosOffice') }}</p>
                  <ul>
                    <li>{{ $t('karimuIkotun') }},</li>
                    <li>Sabo, Yaba,</li>
                    <li>Lagos, Nigeria</li>
                  </ul>
                </div>
                <div>
                  <p>{{ $t('ibadanOffice') }}</p>
                  <ul>
                    <li>{{ $t('codeGarageBuilding') }},</li>
                    <li>{{ $t('omolayoBusStop') }}</li>
                    <li>Ibadan, Nigeria</li>
                  </ul>
                </div>
              </div>
            </div>
          </div>
        </section>
      </footer>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      overlayIsVisible: false,
      language: 'en',
      visible: false,
    }
  },
  watch: {
    $route: {
      handler(to, from) {
        document.body.scrollTop = 0
        document.documentElement.scrollTop = 0
        this.$refs.scroll.scrollTop = 0 // Because my scroll layer is not a body, set the scrollTop of the scroll layer to 0
      },
    },
  },
  methods: {
    showOverlay() {
      console.log('CLICKED')
      if (!this.overlayIsVisible) {
        this.overlayIsVisible = true
      } else {
        this.overlayIsVisible = false
      }
    },
    changeLng(lng) {
      this.language = lng
      this.visible = false
      this.$i18n.setLocale(lng)
      // switchLocalePath(lng)
    },
    showSelectField() {
      this.visible = !this.visible
    },
  },
}
</script>
<style lang="scss" scoped>
.languageSelected {
  margin: 0 1rem;
  margin-left: 2rem;
}
.arrow-down {
  width: 0.875rem;
  img {
    width: 100%;
  }
}
.select_container {
  position: relative;
  .select {
    position: absolute;
    text-align: center;
    .desktop_lang_link {
      border: none;
      outline: none;
      margin: 0.5rem;
      background: transparent;
      color: $primary-color;
      font-family: $nunito;
      font-size: 1rem;
      &:hover {
        color: $gold;
      }
    }
  }
}
</style>
