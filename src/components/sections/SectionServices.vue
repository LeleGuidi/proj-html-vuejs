<template>
  <section class="services">
    <div class="services_container">
        <div class="services_cards">
            <BaseCardBorderRadius class="base_card" v-for="(service, i) in services" :key="i" :items="service"/>
        </div>
        <div class="services_motivation">
            <h2>"How you respond to the challenge in the second half will determine what you become after the game, whether you are a winner or a loser."</h2>
            <BaseSeparator class="separator"/>
            <div class="cit">
                <img class="cit_profile_img" src="../../assets/img/avatar-1-2x.jpg" alt="Brad Johnson"> 
                <h6>Brad Johnson</h6>
                <span>Las Vegas</span>
            </div>
        </div>
    </div>
  </section>
</template>

<script>
import BaseCardBorderRadius from '../commons/BaseCardBorderRadius.vue'
import BaseSeparator from '../smallCommons/BaseSeparator.vue'
export default {
  components: { BaseCardBorderRadius, BaseSeparator },
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
                    title: 'Team training',
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
    // Applicato e padding 
    padding: 0 0 6rem 0;
    @include paddingX;
    // Applicato sfondo effeto sfumatura 
    background: rgb(65,84,254);
    background: linear-gradient(150deg, rgba(65,84,254,1) 10%, rgba(107,12,122,1) 50%, rgba(188,4,40,1) 90%);

    // Al container generico applicata larghezza con margine e proprietà flex 
    &_container {
        @include MainContainer;
        @include FlexColumnBetween;

    }

    
    &_cards {
        // Applicata larghezza e proprietà flex 
        width: 100%;
        @include FlexRowBetween;
        gap: 2rem;
        // Al container delle card applicata posizione relativa per spostarlo verticalmente più sopra 
        position: relative;
        top: -3.125rem;

        .base_card {
            // Applicata una larghezza calcolata in base alle 3 card disponibili 
            width: calc(100% / 3 - 0.66rem);
            padding-bottom: 35%;
            position: relative;
            // Box shadow per effetto interno nella parte inferiore del componenete
            @include cardBoxShadow;
        }
    }
    &_motivation {
        padding: 5rem 10rem;
        text-align: center;

        h2 {
            color: var(--white);
        }
        .separator {
            padding: 2rem;
        }

        .cit {
            @include FlexRowBetween;
            justify-content: center;
            gap: 1rem;

            &_profile_img {
                width: 3rem;
                border-radius: 50%;
            }

            h6 {
                color: var(--white);
            }

            span {
                color: var(--silver);
                font-size: 0.9rem;
            }
        }
    }
}
</style>