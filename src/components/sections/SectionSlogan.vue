<template>
  <section class="slogan">
    <div class="container_small">
        <h2>"I've failed over and over again in my life. And that is why I succeed."</h2>
        <BaseSeparator/>
        <p>Arcu auctor gravid nisl, congue sit nisi tincidunt eget. In lacinia lacus donex sed messa in ipsum eros, tristique. Gravida suspendisse etiam in iaculis.</p>
        <button>Buy Avada today <i class="fa-solid fa-angle-right"></i></button>
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
.slogan {
    padding: 6.2rem 0;
    background: linear-gradient(0deg, rgba(0,0,0,1) 0%, rgba(0,0,0,0) 100%), url("../../assets/img/banner2-2x.jpg");
    background-position: center;
    background-size: cover;
    .container_small {
        @include SmallContainer;
        @include FlexColumnBetween;
        gap: 2rem;
        text-align: center;
    }
    h2 {
        color: var(--white);
        font-size: 2.3rem;
    }
    p {
        color: var(--white);
    }
    button {
        @include ButtonStyle;
        @include ButtonColorBlu;
        padding-left: 3rem;
        padding-right: 3rem;
    }
}
</style>