<template>
    <div class="title_row">
        <h5>{{title}}</h5>
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
    padding: 0 2rem 2rem 0;

    a {
        font-size: small;
        color: inherit;
    }
}
</style>