<template>
    <section class="video">
        <div class="video_max_container">
            <div class="top_row">
                <div class="col">
                    <BaseCardBorderRadius :items="mainVideo" class="main_video"/>
                </div>
                <div class="col">
                    <h5>Tune up your workouts</h5>
                    <h2>The best health & fitness advice online </h2>
                    <BaseYoutubeChannelBtn/>
                    <p>Arcu eu facilisi ut quisque placerat nunc habitant. Magna semper mauris, venenatis, leo integer sit pellentesque.</p>
                    <button class="visit_youtube"><i class="fa-brands fa-youtube"></i> Visit my Youtube channel</button>
                </div>
            </div>
            <div class="video_container">
                <BaseTitleRow title="Featured playlist" link="View all videos"/>
                <div class="bottom_row">
                    <div v-for="(video, i) in videos" :key="i" class="col">
                        <BaseCardBorderRadius :items="video" class="videos"/>
                        <h6>{{video.video_title}}</h6>
                        <span>{{video.video_subtitle}}</span>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import BaseCardBorderRadius from '../commons/BaseCardBorderRadius.vue'
import BaseTitleRow from '../commons/BaseTitleRow.vue'
import BaseYoutubeChannelBtn from '../smallCommons/BaseYoutubeChannelBtn.vue'

export default {
    components: { BaseCardBorderRadius, BaseYoutubeChannelBtn, BaseTitleRow },
    name: 'SectionVideo',
    data() {
        return {
            mainVideo: {
                path: require('../../assets/img/service15-2x.jpg'),
                play_button: true,
                play_button_size: 'medium',
            },
            videos: [
                {
                    path: require('../../assets/img/video2-2x.jpg'),
                    video_title: 'Thighs & glute workout',
                    video_subtitle: 'Increase your mobility',
                    play_button: true,
                    play_button_size: 'small',
                },
                {
                    path: require('../../assets/img/video7-2x.jpg'),
                    video_title: 'Lift, firm & perk up',
                    video_subtitle: 'Feel young again',
                    play_button: true,
                    play_button_size: 'small',
                },
                {
                    path: require('../../assets/img/video9-2x.jpg'),
                    video_title: 'Slim & trim your waist',
                    video_subtitle: 'Shed those extra pounds',
                    play_button: true,
                    play_button_size: 'small',
                },
            ]
        }
    }
}
</script>

<style lang="scss">
@import '../../assets/style/_mixins.scss';
.video {
    background-color: var(--white);

    &_max_container {
        width: 100%;
        .top_row {
            @include FlexRowBetween;
            align-items: flex-start;
            gap: 6rem;

            .col {
                width: calc(100% / 2 - 3rem);
            }
            .main_video {
                padding-bottom: 95%;
                @include cardBoxShadow;

                position: relative;
                top: -9.125rem;
                left: -1rem;
            }
            .col:last-child {
                @include FlexColumnBetween;
                align-items: flex-start;
                gap: 1.5rem;
                padding-right: 4rem;

                h5 {
                    color: var(--royal-blue);
                }
                h2 {
                    font-size: 3rem;
                }
                p {
                    color: var(--jumbo);

                }
                .visit_youtube {
                    @include ButtonStyle;
                    @include ButtonColorRed;
                }
            }
            
            
            
        }
    }

    &_container {
        @include MainContainer;

        .bottom_row {
            @include FlexRowBetween;
            width: 100%;
            gap: 2rem;

            .col {
                width: calc(100% / 3);
                text-align: center;
            }
            .videos {
                padding-bottom: 60%;
                margin-bottom: 1.5rem;
                text-align: left;
            }
            h6 {
                padding-bottom: 0.3rem;
            }
            span {
                color: var(--dodger-blu);
                font-size: small;
            }
        }
    }
    
}

</style>