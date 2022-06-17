<template>
    <div class="title_row">
        <h4>{{title}}</h4>
        <a href="#/">{{link}} <i class="fa-solid fa-angle-right"></i></a>
    </div>
</template>

<script>
export default {
name: 'BaseTitleRow',
props: {
    title: String,
    link: String,
}
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/_mixins.scss';
.title_row {
    @include FlexRowBetween;
    padding: 0 1rem 2rem 0;

    h4 {
        font-weight: 400;
        font-size: 1.3rem;
    }
    a {
        text-decoration: none;
        font-size: small;
        color: inherit;
    }
}
</style>