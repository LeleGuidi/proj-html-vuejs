<template>
  <footer>
    <FooterTop/>
    <hr>
    <FooterBottom/>
  </footer>
</template>

<script>
import FooterBottom from '../sections/FooterBottom.vue'
import FooterTop from '../sections/FooterTop.vue'
export default {
  components: { FooterTop, FooterBottom },

}
</script>

<style lang="scss" scoped>
footer {
    background-color: var(--cod-gray);
    width: 100%;

    hr {
        border: .0025rem solid var(--jumbo);
    }
}
</style>