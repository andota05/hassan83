<template>
  <img
    class="image"
    :src="imageSrc"
    :alt="altText"
  >
</template>

<script>
export default {
  name: 'BaseImage',
  props: {
    imageSrc: String,
    altText: String
  }
}
</script>

<style lang="scss" scoped>
.image {
  width: 100%;
  max-width: 100%;
}
</style>
