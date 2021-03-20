<template>
  <div>
    <vsa-list :init-active="initIsTrue">
      <vsa-item>
        <vsa-heading
          ><span class="accordion_heading">{{ heading }}</span>
          <div class="tiny-border">
            <span></span>
            <span></span>
            <span></span>
            <span></span>
          </div>
        </vsa-heading>
        <vsa-icon>
          <span class="open">
            <img src="@/assets/img/icon/arrow-up.svg" alt="arrow-up" />
          </span>
          <span class="close">
            <img src="@/assets/img/icon/arrow-down.svg" alt="arrow-up" />
          </span>
        </vsa-icon>

        <vsa-content><slot name="content"></slot></vsa-content>
      </vsa-item>
    </vsa-list>
  </div>
</template>
<script>
import {
  VsaList,
  VsaItem,
  VsaHeading,
  VsaContent,
  VsaIcon,
} from 'vue-simple-accordion'
export default {
  name: 'AppAccordion',
  components: {
    VsaList,
    VsaItem,
    VsaHeading,
    VsaContent,
    VsaIcon,
  },
  props: {
    heading: {
      type: String,
      default: '',
    },
    initIsTrue: {
      type: Boolean,
      default: false,
    },
  },
}
</script>
