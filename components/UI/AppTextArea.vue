<template>
  <div class="full-input">
    <span>
      <img :src="getImgUrl(iconPath)" alt="arrow-up" />
    </span>
    <textarea
      v-model="innerValue"
      type="text"
      :placeholder="placeholder"
      cols="50"
      rows="4"
    />
  </div>
</template>
<script>
export default {
  name: 'AppTextArea',
  props: {
    value: {
      type: String,
      default: '',
    },
    placeholder: {
      type: String,
      default: '',
    },
    iconPath: {
      type: String,
      default: '',
    },
  },
  data() {
    return {
      innerValue: '',
    }
  },
  watch: {
    value: {
      handler(newVal, oldVal) {
        if (newVal && (newVal !== '' || newVal.length > 0)) {
          this.innerValue = newVal
        } else {
          this.innerValue = undefined
        }
      },
      immediate: true,
    },
    innerValue: {
      handler(newVal, oldVal) {
        this.$emit('input', this.innerValue)
      },
      immediate: true,
    },
  },
  methods: {
    getImgUrl(pic) {
      return require('~/assets/img/icon/' + pic)
    },
  },
}
</script>
<style lang="scss" scoped>
.full-input {
  display: flex;
  width: 100%;
  background: $dark-grey;
  padding: 0.5rem $s16;
  border: 1.5px solid rgba(157, 157, 157, 0.24);
  margin-bottom: $s16;
  border-radius: 0.5rem;
  span {
    width: 1.166875rem;
    height: 1.166875rem;
    img {
      width: 100%;
      height: 100%;
    }
  }
}
textarea {
  outline: none;
  border: none;
  display: block;
  font-family: $nunito-sans;
  font-style: normal;
  font-weight: 700;
  font-size: $s16;
  line-height: $s24;
  width: 100%;
  background: transparent;
  color: $primary-color;
  margin-left: 0.5rem;
}
textarea,
textarea::before,
textarea::after {
  -webkit-user-select: initial;
  -moz-user-select: initial;
  -ms-user-select: initial;
  user-select: initial;
}
</style>
