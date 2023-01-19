<template>
  <component :is="tagName" :class="className">
    <slot></slot>
  </component>
</template>

<script>
export default {
  name: 'BaseHeadeing',
  props: {
    tag: {
      type: String,
      required: true
    },
    className: String
  },
  computed: {
    tagName() {
      return this.tag
    },
  }
}
</script>

<style lang="scss" scoped>

</style>
