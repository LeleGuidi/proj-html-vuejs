<template>
  <section class="plan">
    <div class="plan_container">
        <div class="row">
          <BaseCardPlan v-for="(plan, i) in plans" :key="i" :items="plan"/>        
        </div>
    </div>
  </section>
</template>

<script>
import BaseCardPlan from '../commons/BaseCardPlan.vue'
export default {
  components: { BaseCardPlan },
  name: 'SectionPlan',
  data() {
    return{
      plans: [
        {
          path: require('../../assets/img/orologio.png'),
          title: 'Team training',
          subtitle: 'Find a partner',
          details: 'Vestibilum, curabitur eu sem nibh ultrices sit nulla adipiscing. Nisl sit fames amet senectus eget sed duis vehicula. Tristique.',
          link: 'Find a partner',
        },
        {
          path: require('../../assets/img/peso.png'),
          title: 'Crossfit workout',
          subtitle: 'Push your limits',
          details: 'Vestibilum, curabitur eu sem nibh ultrices sit nulla adipiscing. Nisl sit fames amet senectus eget sed duis vehicula. Tristique.',
          link: 'Learn about crossfit',
        },
        {
          path: require('../../assets/img/perdipeso.png'),
          title: 'Weight loss plan',
          subtitle: 'Shed those pounds',
          details: 'At laoreet senectus volutpat diam vel sed sed amet pellentesque. Lobortis ut aliquam risus purus. A tellus ut etiam.',
          link: 'Schedule a workout',
        },
      ]
    }
  }
}
</script>

<style lang="scss" scoped> 
@import '../../assets/style/_mixins.scss';
.plan {
  background-color: var(--cod-gray);
  width: 100%;
  padding: 5rem 0;
  &_container {
    @include MainContainer;
  }
  .row {
    @include FlexRowBetween;
    gap: 3rem;
    align-items: stretch;
  }
}
</style>