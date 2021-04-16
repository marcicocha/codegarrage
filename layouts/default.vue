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
          <nuxt-link to="about"><span>About</span></nuxt-link>
          <nuxt-link to="services"><span>Services</span></nuxt-link>
          <nuxt-link to="portfolio"><span>Portfolio</span></nuxt-link>
        </div>

        <nuxt-link to="contact" class="button header__button hide-for-mobile"
          >CONTACT US</nuxt-link
        >
      </nav>
      <div
        :class="{
          header__menu: true,
          'fade-in': overlayIsVisible,
          'fade-out': !overlayIsVisible,
        }"
      >
        <div @click="showOverlay">
          <nuxt-link to="about"><span>About</span></nuxt-link>
        </div>
        <div @click="showOverlay">
          <nuxt-link to="services"><span>Services</span></nuxt-link>
        </div>
        <div @click="showOverlay">
          <nuxt-link to="portfolio"><span>Portfolio</span></nuxt-link>
        </div>
        <div @click="showOverlay">
          <nuxt-link to="contact" class="button header__button"
            >CONTACT US</nuxt-link
          >
        </div>
      </div>
    </header>
    <div class="child-body">
      <div>
        <Nuxt />
      </div>

      <footer class="footer">
        <section class="container flex flex-jc-sb flex-ai-c">
          <h2>
            We collaborate with ambitious brands and people; Let’s build
            something great together.
          </h2>
          <div>
            <nuxt-link to="contact" class="button">CONTACT US</nuxt-link>
          </div>
        </section>
        <section class="container">
          <div class="border flex">
            <div class="footer__logo">
              <img src="@/assets/img/logo.svg" alt="logo-white" />
              <p>CodegarrageAfrica</p>
            </div>
            <div class="footer__details">
              <div class="footer__details_lists flex">
                <div>
                  <p>Explore</p>
                  <ul>
                    <li>
                      <nuxt-link to="about"><span>About</span></nuxt-link>
                    </li>
                    <li>
                      <nuxt-link to="services"><span>Services</span></nuxt-link>
                    </li>
                    <li>
                      <nuxt-link to="portfolio"
                        ><span>Portfolio</span></nuxt-link
                      >
                    </li>
                    <li>
                      <nuxt-link to="career"><span>Careers</span></nuxt-link>
                    </li>
                    <li>
                      <nuxt-link to="portfolio"
                        ><span>Testimonials</span></nuxt-link
                      >
                    </li>
                  </ul>
                </div>
                <div>
                  <p>Contact</p>
                  <ul>
                    <li>services@codegarage.africa</li>
                    <li>08185956620</li>
                  </ul>
                </div>
                <div>
                  <p>Follow</p>
                  <ul>
                    <li>
                      <a
                        href="https://twitter.com/CodegarageA"
                        target="_blank"
                      ></a>
                      Twitter
                    </li>
                    <li>
                      <a
                        href="https://www.instagram.com/386konsult"
                        target="_blank"
                        >Instagram</a
                      >
                    </li>
                    <li>
                      <a
                        href="https://www.linkedin.com/company/386konsult"
                        target="_blank"
                        >LinkedIn</a
                      >
                    </li>
                  </ul>
                </div>
                <div>
                  <p>Legal</p>
                  <ul>
                    <li>Terms</li>
                    <li>Privacy</li>
                  </ul>
                </div>
                <div>
                  <p>Lagos Office</p>
                  <ul>
                    <li>10, Karimu Ikotun close,</li>
                    <li>Sabo, Yaba,</li>
                    <li>Lagos, Nigeria</li>
                  </ul>
                </div>
                <div>
                  <p>Ibadan Office</p>
                  <ul>
                    <li>CodeGarrage Building,</li>
                    <li>Omolayo Bus-Stop, Akobo</li>
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
    }
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
  },
}
</script>
