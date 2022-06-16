<template>
    <div>
        <button class="btn_play"><i class="fa-solid fa-play"></i></button>
    </div>
</template>
<script>
export default {

}
</script>

<style lang="scss">
@import '../../assets/style/_mixins.scss';
div {
    .btn_play {
        @include ButtonPlay;
    }
}
</style>