<template>
    <div class="card" :style="'background-image: url('+items.path+')'">
        <BaseSeparator class="separator" v-show="(items.separator == true)"/>
        <h3 v-show="(items.title)">{{items.title}}</h3>
        <span v-show="(items.subtitle)">{{items.subtitle}}</span>
    </div>
</template>

<script>
import BaseSeparator from './BaseSeparator.vue'
export default {
  components: { BaseSeparator },
    name: 'BaseCard',
    props: {
        items: Array,
    }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/_mixins.scss';
.card {
    padding: 1.5rem;
    border-radius: .1825rem;
    border-bottom-right-radius: 1.25rem;
    background-size: cover;

    @include FlexColumnBetween;
    justify-content: end;
    align-items: start;

    .separator {
        color: var(--white);
        padding-bottom: 1rem;
    }
    h3 {
        color: var(--white);
    }
    span {
        color: var(--yellow);
    }
    

}
</style>