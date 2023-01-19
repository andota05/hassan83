<template>
  <header class="header">
    <div class="header__logo">
      <base-logo />
    </div>
  </header>
</template>

<script>
import BaseLogo from '/src/components/molecules/BaseLogo.vue'

export default {
  name: 'TheHeader',
  components: {
    BaseLogo
  },
}
</script>

<style scoped>
.header {
  display: flex;
  justify-content: center;
}
</style>
