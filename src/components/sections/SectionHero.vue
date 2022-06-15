<template>
  <section class="hero">
    <div class="hero_container">
        <div class="title">
            <h4>Certified fitness professional</h4>
            <h1>Take control of your health</h1>
            <BaseSeparator/>
            <span>Curabitur non nulla sit amet nisl tempus convallis quis ac lectus dolor sit amet.</span>
            <div class="cta_button">
                <button class="visit_youtube"><i class="fa-brands fa-youtube"></i> Visit my Youtube channel</button>
                <button class="buy_now">Buy Avada today <i class="fa-solid fa-arrow-right"></i></button>
            </div>
        </div>
        <div class="play_button">
            <button class="btn_play"><i class="fa-solid fa-play"></i></button>
        </div>
    </div>
  </section>
</template>

<script>
import BaseSeparator from '../commons/BaseSeparator.vue'
export default {
  components: { BaseSeparator },

}
</script>

<style lang="scss" scoped>
@import '../../assets/style/_mixins.scss';
.hero {
    background: linear-gradient(90deg, rgba(6,6,6,1) 47%, rgba(6,6,6,0.6124824929971988) 53%, rgba(6,6,6,0) 72%), url("../../assets/img/slider82x-scaled.jpg");
    background-position: center top;
    background-size: cover;
    width: 100%;
    padding: 7rem 1rem;

    &_container {
        @include MainContainer;
        @include FlexRowBetween;
    }
    
    .title {
        @include FlexColumnBetween;
        align-items: start;
        gap: 1.2rem;
        flex-flow: 1;

        h4 {
            color: var(--burnt-sienna);
            font-size: 1.25rem;
        }
        h1 {
            font-size: 3.4375rem;
            color: var(--white);
        }
        .separatore {
            color: var(--yellow);
        }
        span {
            color: var(--jumbo);
        }
        .cta_button {
            padding: 1rem 0;
            button {
                @include ButtonStyle;
                margin-right: 1rem;
            }
            button.visit_youtube {
                @include ButtonColorBlu;
            }
            button.buy_now {
                @include ButtonColorBlack;
            }
        }  
    }

    .play_button {
        flex-grow: 0.9;
        text-align: center;

        .btn_play {
            @include ButtonPlay
        }
    }
}
</style>