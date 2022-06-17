<template>
    <section class="training">
        <div class="training_container">
            <div class="row">
                <BasePlayButton class="play"/>
                <h2>Crossfit workout of the day</h2>
                <p>November 15th, 2019</p>
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
    width: 100%;
    padding: 7rem 0;
    background: linear-gradient(150deg, rgba(65,84,254,0.4) 10%, rgba(107,12,122,0.4) 50%, rgba(188,4,40,0.4) 90%), url('../../assets/img/banner14-2x.jpg');
    background-position: center;
    background-size: cover;

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
        p {
            color: var(--yellow);
            font-size: 1.6rem;
            font-weight: bold;
        }
        a {
            color: var(--white);
            text-decoration: none;

            .arrow {
                vertical-align: middle;
            }
        }
    }
}
</style>