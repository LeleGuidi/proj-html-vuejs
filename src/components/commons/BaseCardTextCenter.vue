<template>
  <div class="card_plan">
    <img :src="items.path" :alt="items.title">
    <BaseSeparator v-show="(items.separator == true)" class="separator"/>
    <div class="title">
        <h3 v-show="(items.title)">{{items.title}}</h3>
        <h4 v-show="(items.subtitle)">{{items.subtitle}}</h4>
    </div>
    <p class="details">{{items.details}}</p>
    <a class="link" href="#/">{{items.link}} <i class="fa-solid fa-angle-right"></i></a>
  </div>
</template>

<script>
import BaseSeparator from '../smallCommons/BaseSeparator.vue'
export default {
  components: { BaseSeparator },
    name: 'BaseCardPLanTextCenter',
    props: {
        items: Object,
    }
}
</script>

<style lang="scss">
@import '../../assets/style/_mixins.scss';
.card_plan {
    background-color: var(--cod-gray);
    border: .125rem solid var(--royal-blue);
    border-radius: .625rem;
    padding: 3rem 3rem;
    text-align: center;

    @include FlexColumnBetween;
    gap: 2rem;
    img {
        width: 5.875rem;
    }
    .separator {
        color: var(--royal-blue);
    }
    h3 {
        color: var(--white);
        padding-bottom: 0.4rem;
    }
    h4 {
        color: var(--yellow);
    }

    h3, h4 {
        font-weight: 500;
    }
    p {
        color: var(--silver);
    }
    a {
        color: var(--white);
        font-weight: 500;
        font-size: .9rem;
        text-decoration: none;
    }
}
</style>