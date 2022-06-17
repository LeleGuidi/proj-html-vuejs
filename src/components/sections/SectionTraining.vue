<template>
    <section class="training">
        <div class="training_container">
            <div class="row">
                <BasePlayButton class="play"/>
                <h2>Crossfit workout of the day</h2>
                <h4>November 15th, 2019</h4>
                <a href="#/">View all videos <i class="arrow fa-solid fa-arrow-right-long"></i></a>
            </div>
        </div>
    </section>
</template>

<script>
import BasePlayButton from "../smallCommons/BasePlayButton.vue"

export default {
  components: { BasePlayButton }

}
</script>

<style lang="scss" scoped>
@import '../../assets/style/_mixins.scss';
.training {
    background: linear-gradient(150deg, rgba(0, 11, 114, 0.5) 10%, rgba(92, 4, 106, 0.5) 50%,rgba(123, 3, 27, 0.5) 90%), url('../../assets/img/banner14-2x.jpg');
    background-position: center;
    background-size: cover;
    padding: 8rem 1rem;

    &_container {
        @include SmallContainer;

        .row {
            @include FlexColumnBetween;
            gap: 1rem;
        }

        .play{
            transform: scale(0.8);
        }

        h2 {
            color: var(--white);
            font-size: 2.6rem;
            font-weight: 500;
        }
        h4 {
            color: var(--yellow);
        }
        a {
            color: var(--white);

            .arrow {
                vertical-align: middle;
            }
        }
    }
}
</style>