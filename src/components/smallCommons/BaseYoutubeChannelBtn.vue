<template>
    <div class="youtube_channel">
        <img class="youtube_channel_logo" src="../../assets/img/unnamed.jpg" alt="Logo Youtube Channel">
        <div class="youtube_channel_link">
            <span class="youtube_channel_link_name">ThemeFusion</span>
            <div class="youtube_channel_link_btn">
                <button><i class="fa-brands fa-youtube"></i> YouTube </button>
                <span>999+</span>
            </div>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
@import '../../assets/style/_mixins.scss';
.youtube_channel {
    @include FlexRowBetween;
    align-items: flex-end;
    gap: 0.3rem;

    &_link {
        @include FlexColumnBetween;
        gap: 0.3rem;
        align-items: flex-start;

        &_logo {
            flex-grow: 1;
            height: 100%;
        }

        &_name {
            color: var(--silver);
            font-size: .625rem;
            font-weight: 500;
        }

        &_btn {
            @include FlexRowBetween;
            button {
                color: var(--white);
                background-color: #e62117;
                border: none;
                font-size: 0.625rem;
                font-weight: 600;
                vertical-align: bottom;
                padding: .1875rem;
            }
            span {
                font-size: 0.625rem;
                color: var(--silver);
                font-weight: 500;
                border: .063rem solid var(--silver);
                border-left: none;
                padding-bottom: .0619rem;
                padding-left: .125rem;
            }
            
        }
    }
}
</style>