<template>
  <div class="logo">
    <base-image :imageSrc="logoFile" altText="発散サイト" />
  </div>
</template>

<script>
import BaseImage from '@/components/atoms/BaseImage.vue'

import { LOGO_FILE } from '@/constant.js'

export default {
  name: 'BaseLogo',
  components: {
    BaseImage
  },
  data() {
    return {
      logoFile: require(`@/assets/${LOGO_FILE}`)
    }
  }
}
</script>

<style lang="scss" scoped>
  .logo {
    width: 200px;
  }
</style>
