<template>
<main>
    <SectionHero/>
    <SectionServices/>
    <SectionVideo/>
    <SectionMailing/>
</main>
</template>

<script>
import SectionHero from '../sections/SectionHero.vue'
import SectionMailing from '../sections/SectionMailing.vue'
import SectionServices from '../sections/SectionServices.vue'
import SectionVideo from '../sections/SectionVideo.vue'
export default {
  components: { SectionHero, SectionServices, SectionVideo, SectionMailing },

}
</script>

<style>

</style>