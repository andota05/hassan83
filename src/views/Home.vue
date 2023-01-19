<template>
  <main class="main">
    <the-header />

    <section class="section">
      <h1 class="section__title">思う存分、枠内をクリックしてください</h1>
      
      <div class="click-space" @click="onClickArea()">
        <p class="click-space__message">{{ message }}</p>
      </div>
    </section>
  </main>
</template>

<script>
import TheHeader from '/src/components/organism/Header.vue'

export default {
  name: 'Home',
  components: {
    TheHeader
  },
  props: {
    msg: String
  },
  data() {
    return {
      clicked: 0,
      message: ''
    }
  },
  methods: {
    onClickArea() {
      this.clicked++
      this.message = this.generateMessage(this.clicked)
    },
    generateMessage(clickCount) {
      const message = clickCount % 2 === 0 ? '8' : '3'
      return message
    }
  },
}
</script>

<style lang="scss" scoped>
.section {
  &__title {
    font-size: 16px;
  }
}
.click-space {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 300px;
  height: 400px;
  border: 1px solid #42b983;
  margin: 0 auto;
  cursor: pointer;

  &__message {
    margin: 0 auto;
    max-height: 100%;
    font-size: 200px;
  }
}
</style>
