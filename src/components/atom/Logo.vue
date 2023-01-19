<template>
  <div class="logo">
    <img class="logo__image" :src="require(`@/assets/${logo}`)">
  </div>
</template>

<script>
import { LOGO_FILE } from '/src/constant.js'

export default {
  name: 'Logo',
  data() {
    return {
      logo: LOGO_FILE
    }
  }
}
</script>

<style lang="scss" scoped>
.logo {
  &__image {
    max-width: 100%;
  }
}
</style>
