<template>
<main>
    <SectionHero/>
    <SectionServices/>
    <SectionVideo/>
    <SectionMailing/>
    <SectionPlan/>
    <SectionArticles/>
    <SectionSlogan/>
</main>
</template>

<script>
import SectionArticles from '../sections/SectionArticles.vue'
import SectionHero from '../sections/SectionHero.vue'
import SectionMailing from '../sections/SectionMailing.vue'
import SectionPlan from '../sections/SectionPlan.vue'
import SectionServices from '../sections/SectionServices.vue'
import SectionSlogan from '../sections/SectionSlogan.vue'
import SectionVideo from '../sections/SectionVideo.vue'

export default {
  components: { 
    SectionHero, 
    SectionServices, 
    SectionVideo, 
    SectionMailing,
    SectionPlan,
    SectionArticles,
    SectionSlogan
  },

}
</script>

<style>

</style>