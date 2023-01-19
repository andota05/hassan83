<template>
  <main class="main">
    <section class="section">
      <base-heading tag="h1"  class="section__title">
        思う存分、枠内をクリックしてください
      </base-heading>
      
      <div class="click-space" @click="onClickArea()">
        <div class="click-space__message" v-for="(message, index) in messages" :key="index">
          <p class="message">{{ message }}</p>
        </div>
      </div>
    </section>
  </main>
</template>

<script>
import BaseHeading from '@/components/atoms/BaseHeading.vue'

export default {
  name: 'HomePage',
  components: {
    BaseHeading
  },
  data() {
    return {
      clicked: 0,
      messages: []
    }
  },
  methods: {
    onClickArea() {
      this.clicked++
      this.messages = this.generateMessage(this.clicked)
    },
    generateMessage(clickCount) {
      const messages = clickCount % 2 === 0 ? ['3'] : ['8']
      return messages
    }
  },
}
</script>

<style lang="scss" scoped>
.main {
  padding: 24px 0;
  display: flex;
  flex-direction: column;
}
.section {
  display: flex;
  flex-direction: column;
  gap: 12px;

  &__title {
    font-size: 16px;
  }
}
.click-space {
  display: flex;
  width: 300px;
  height: 300px;
  border: 1px solid #42b983;
  margin: 0 auto;
  cursor: pointer;

  &__message {
    display: flex;
    align-items: center;
    flex-grow: 1;
  }
}
.message {
  margin: 0 auto;
  max-width: 100%;
  max-height: 100%;
  font-size: 200px;
}
</style>
