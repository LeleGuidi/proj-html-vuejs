<template>
    <header class="header">
        <div class="header_row">
            <div class="header_img">
                <img src="../../assets/img/logo-2x.png" alt="Logo Avada Fitness">
            </div>
            <div class="header_navbar">
                <BaseNavbar/>
            </div>
            <div class="header_right">
                <button>Schedule a workout</button>
                <i class="icon fa-solid fa-cart-shopping"></i>
                <i class="icon fa-solid fa-magnifying-glass"></i>
            </div>
        </div>
    </header>
</template>

<script>
import BaseNavbar from '../commons/BaseNavbar.vue'
export default {
  components: { BaseNavbar },

}
</script>

<style lang="scss" scoped>
@import '../../assets/style/_mixins.scss';
.header {
    background-color: var(--cod-gray);
    padding: .9375rem 0;
    width: 100%;
    &_row {
        @include MainContainer;
        @include FlexRowBetween;
        gap: 2.5rem;
    }
    &_img {
        flex-grow: 1;
        img {
            width: 15rem;
        }
    }
    &_right {
        @include FlexRowBetween;
        gap: 2.5rem;
        button {
            @include ButtonStyle;
            background-color: var(--dodger-blu);
            border: .0625rem solid var(--dodger-blu);
            color: var(--white);
        }
        .icon {
            color: var(--jumbo);
        }
    }
}
</style>