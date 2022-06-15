<template>
  <div id="app">
    <BaseHeader/>
    <BaseFooter/>
  </div>
</template>

<script>
import BaseFooter from './components/blocks/BaseFooter.vue'
import BaseHeader from './components/blocks/BaseHeader.vue'


export default {
  name: 'App',
  components: {
    BaseHeader,
    BaseFooter

  }
}
</script>

<style lang="scss">
@import url('../src/assets/globals.scss');
</style>
