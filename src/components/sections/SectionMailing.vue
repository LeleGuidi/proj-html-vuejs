<template>
  <section class="hero">
    <div class="hero_container">
        <div class="title">
            <h4>Join our mailing list today</h4>
            <h2>Insider offers & flash sales in your inbox every week.</h2>
            <BaseSeparator/>
            <div class="cta_button">
                <input class="email_input" type="email" placeholder="Insert your email ...*">
                <button class="subscribe">Subscribe</button>
            </div>
            <span>Curabitur non nulla sit amet nisl tempus convallis quis ac lectus dolor sit amet, consectetur adipiscing elit sed porttitor lectus.</span>
        </div>
    </div>
  </section>
</template>

<script>
import BaseSeparator from '../commons/BaseSeparator.vue'
export default {
  components: { BaseSeparator},

}
</script>

<style lang="scss" scoped>
@import '../../assets/style/_mixins.scss';
.hero {
    background: linear-gradient(90deg, rgba(6,6,6,1) 47%, rgba(6,6,6,0.6124824929971988) 53%, rgba(6,6,6,0) 72%), url("../../assets/img/banner1-2x.jpg");
    background-position: center top;
    background-size: cover;
    width: 100%;
    padding: 7rem;
    
    &_container {
        @include MainContainer;
    }
    
    .title {
        @include FlexColumnBetween;
        align-items: start;
        gap: 1.2rem;
        width: 70%;

        h4 {
            color: var(--burnt-sienna);
            font-size: 1.10rem;
            font-weight: 500;
        }
        h2 {
            font-size: 2.7rem;
            font-weight: 500;
            color: var(--white);
            padding-right: 1rem;
        }
        .separatore {
            color: var(--yellow);
        }
        span {
            color: var(--jumbo);
            padding-right: 1rem;
        }
        .cta_button {
            width: 100%;
            padding: 1rem 0;
            button.subscribe {
                @include ButtonColorBlu;
                @include ButtonStyle;
                margin-left: 1.7rem;
                padding-left: 5rem;
                padding-right: 5rem;
            }
            .email_input {
                @include InputText;
                width: 65%;

            }
        }  
    }
}
</style>