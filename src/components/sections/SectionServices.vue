<template>
  <section class="services">
    <div class="services_container">
        <div class="services_cards">
            <BaseCard class="base_card" v-for="(service, i) in services" :key="i" :items="services[i]"/>
        </div>
        <div class="services_review">
            <h2>"How you respond to the challenge in the second half will determine what you become after the game, whether you are a winner or a loser."</h2>
        </div>
    </div>
  </section>
</template>

<script>
import BaseCard from '../commons/BaseCard.vue'
export default {
  components: { BaseCard },
    name: 'SectionServices',
    data() {
        return {
            services: [
                {
                    title: 'Crossfit workout',
                    subtitle: 'Push your limits',
                    separator: true,
                    path: require('../../assets/img/service6-2x.jpg'),
                },
                {
                    title: 'New gym apparel',
                    subtitle: 'Look good, feel good',
                    separator: true,
                    path: require('../../assets/img/box1-2x.jpg'),
                },
                {
                    title: 'Crossfit workout',
                    subtitle: 'Find a partner',
                    separator: true,
                    path: require('../../assets/img/box3-2x.jpg'),
                }
            ]
        }
    }
}
</script>

<style lang="scss">
@import '../../assets/style/_mixins.scss';
.services {
    width: 100%;
    background: rgb(65,84,254);
    background: linear-gradient(150deg, rgba(65,84,254,1) 10%, rgba(107,12,122,1) 50%, rgba(188,4,40,1) 90%);
    height: 43.75rem;

    &_container {
        @include MainContainer;
        position: relative;
        @include FlexColumnBetween;

    }
    &_cards {
        position: absolute;
        top: -3rem;
        left: 0;
        right: 0;
        @include FlexRowBetween;
        gap: 2rem;
        .base_card {
            width: calc(100% / 3);
            height: 22rem;
            box-shadow: inset 0rem -7rem 3.125rem .3125rem rgba(0,0,0,0.48);
        }
    }
}
</style>