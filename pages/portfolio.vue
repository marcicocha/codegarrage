<template>
  <div class="container padding">
    <h6>{{ $t('ourWork') }}</h6>
    <h3 class="column-6">
      {{ $t('portfolioDescription') }}
    </h3>
    <AppYourIdeas />
  </div>
</template>
<script>
import AppYourIdeas from '@/components/indexPage/AppYourIdeas'

export default {
  components: {
    AppYourIdeas,
  },
}
</script>
