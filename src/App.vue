<template>
  <div id="app">
    <BaseHeader/>
    <BaseMain/>
    <BaseFooter/>
  </div>
</template>

<script>
import BaseFooter from './components/blocks/BaseFooter.vue'
import BaseHeader from './components/blocks/BaseHeader.vue'
import BaseMain from './components/blocks/BaseMain.vue'


export default {
  name: 'App',
  components: {
    BaseHeader,
    BaseFooter,
    BaseMain

  }
}
</script>

<style lang="scss">
@import url('../src/assets/globals.scss');
</style>
