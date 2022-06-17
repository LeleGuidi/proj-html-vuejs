<template>
  <section class="mailing">
    <div class="mailing_container">
        <div class="title">
            <h5>Join our mailing list today</h5>
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
import BaseSeparator from '../smallCommons/BaseSeparator.vue'
export default {
  components: { BaseSeparator},

}
</script>

<style lang="scss" scoped>
@import '../../assets/style/_mixins.scss';
.mailing {
    background: linear-gradient(90deg, rgba(6,6,6,1) 47%, rgba(6,6,6,0.6124824929971988) 53%, rgba(6,6,6,0) 72%), url("../../assets/img/banner1-2x.jpg");
    background-position: center top;
    background-size: cover;
    
    &_container {
        @include MainContainer;
    }
    
    .title {
        @include FlexColumnBetween;
        align-items: start;
        gap: 1.2rem;
        width: 66%;

        h5 {
            color: var(--burnt-sienna);
        }
        h2 {
            color: var(--white);
            font-size: 3rem;
        }
        .separatore {
            color: var(--yellow);
        }
        span {
            color: var(--jumbo);
            padding-right: 1rem;
        }
        .cta_button {
            @include FlexRowBetween;
            gap: 2rem;
            width: 100%;
            padding: 1rem 0;
            
            button.subscribe {
                @include ButtonColorBlu;
                @include ButtonStyle;
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