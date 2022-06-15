<template>
  <div class="footer_bottom">
    <p><i class="copyright_icon fa-regular fa-copyright"></i> Copyright 2012 - 2020 | Avada theme by <span>ThemeFusion</span> | All rights reserved | Powered by <span>WordPress</span></p>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss">
@import '../../assets/style/_mixins.scss';
.footer_bottom {
    padding: 1.80rem 0;
    text-align: center;
    color: var(--jumbo);
    font-size: 0.9rem;
    @include MainContainer;

    span {
        color: var(--white);
    }
}
</style>