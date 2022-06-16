<template>
  <div class="card_plan">
    <img :src="items.path" :alt="items.title">
    <div class="title">
        <h3>{{items.title}}</h3>
        <h4>{{items.subtitle}}</h4>
    </div>
    <p>{{items.details}}</p>
    <a href="#/">{{items.link}} <i class="fa-solid fa-angle-right"></i></a>
  </div>
</template>

<script>
export default {
    name: 'BaseCardPLan',
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