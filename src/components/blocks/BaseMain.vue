<template>
<main>
    <SectionHero/>
    <SectionServices/>
    <SectionVideo/>
    <SectionMailing/>
    <SectionPlan/>
    <SectionArticles/>
    <SectionSlogan/>
    <SectionSponsor/>
    <SectionTraining/>
</main>
</template>

<script>
import SectionTraining from '../sections/SectionTraining.vue'
import SectionArticles from '../sections/SectionArticles.vue'
import SectionHero from '../sections/SectionHero.vue'
import SectionMailing from '../sections/SectionMailing.vue'
import SectionPlan from '../sections/SectionPlan.vue'
import SectionServices from '../sections/SectionServices.vue'
import SectionSlogan from '../sections/SectionSlogan.vue'
import SectionSponsor from '../sections/SectionSponsor.vue'
import SectionVideo from '../sections/SectionVideo.vue'

export default {
  components: { 
    SectionTraining,
    SectionHero, 
    SectionServices, 
    SectionVideo, 
    SectionMailing,
    SectionPlan,
    SectionArticles,
    SectionSlogan,
    SectionSponsor
  },

}
</script>

<style>

</style>