<template>
<main>
    <SectionHero/>
    <SectionServices/>
    <SectionVideo/>
    <SectionMailing/>
    <SectionPlan/>
</main>
</template>

<script>
import SectionHero from '../sections/SectionHero.vue'
import SectionMailing from '../sections/SectionMailing.vue'
import SectionPlan from '../sections/SectionPlan.vue'
import SectionServices from '../sections/SectionServices.vue'
import SectionVideo from '../sections/SectionVideo.vue'
export default {
  components: { 
    SectionHero, 
    SectionServices, 
    SectionVideo, 
    SectionMailing,
    SectionPlan
  },

}
</script>

<style>

</style>