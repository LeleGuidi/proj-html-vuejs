<template>
  <div class="card_plan">
    <img :src="items.path" :alt="items.title">
    <BaseSeparator v-show="(items.separator == true)" class="separator"/>
    <div class="title">
        <h5 v-show="(items.title)">{{items.title}}</h5>
        <h6 v-show="(items.subtitle)">{{items.subtitle}}</h6>
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
    padding: 3rem 3.3rem;
    text-align: center;

    @include FlexColumnBetween;
    gap: 2rem;

    &:hover {
        transform: scale(1.05);
    }
    img {
        width: 5.875rem;
    }
    .separator {
        color: var(--royal-blue);
    }
    h5 {
        color: var(--white);
        padding-bottom: 0.4rem;
    }
    h6 {
        color: var(--yellow);
    }
    p {
        color: var(--silver);
        font-size: 0.9rem;
    }
    a {
        color: var(--white);
        font-weight: 500;
        font-size: .9rem;
    }
}
</style>