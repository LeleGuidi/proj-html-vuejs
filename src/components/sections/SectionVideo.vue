<template>
    <section class="video">
        <div class="video_max_container">
            <div class="top_row">
                <div class="col">
                    <BaseCard :items="mainVideo" class="main_video"/>
                </div>
                <div class="col">
                    <h4>Tune up your workouts</h4>
                    <h2>The best health & fitness advice online </h2>
                    <BaseYoutubeChannelBtn/>
                    <p>Arcu eu facilisi ut quisque placerat nunc habitant. Magna semper mauris, venenatis, leo integer sit pellentesque.</p>
                    <button class="visit_youtube"><i class="fa-brands fa-youtube"></i> Visit my Youtube channel</button>
                </div>
            </div>
            <div class="video_container">
                <div class="featured_playlist">
                    <h4>Featured Playlist</h4>
                    <a href="#/">View all videos <i class="fa-solid fa-angle-right"></i></a>
                </div>
                <div class="bottom_row">
                    <div v-for="(video, i) in videos" :key="i" class="col">
                        <BaseCard :items="video" class="videos"/>
                        <h5>{{video.video_title}}</h5>
                        <span>{{video.video_subtitle}}</span>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import BaseCard from '../commons/BaseCard.vue'
import BaseYoutubeChannelBtn from '../commons/BaseYoutubeChannelBtn.vue'
export default {
    components: { BaseCard, BaseYoutubeChannelBtn },
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
    padding-bottom: 6.125rem;

    &_max_container {
        width: 100%;
        .top_row {
            @include FlexRowBetween;
            gap: 6rem;

            .col {
                width: calc(100% / 2 - 3rem);
            }
            .main_video {
                padding-bottom: 95%;
                @include cardBoxShadow;

                position: relative;
                top: -3.125rem;
            }
            .col:last-child {
                @include FlexColumnBetween;
                align-items: flex-start;
                gap: 1.5rem;
                padding-right: 4rem;

                h4 {
                    color: var(--royal-blue);
                    font-weight: 400;
                    font-size: 1.2rem;
                }
                h2 {
                    font-size: 2.5rem;
                    font-weight: 400;
                }
                p {
                    font-weight: 300;
                    color: var(--silver);

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

        .featured_playlist {
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
            h5 {
                padding-bottom: 0.3rem;
                font-weight: 400;
                font-size: 1rem
            }
            span {
                color: var(--dodger-blu);
                font-size: small;
            }
        }
    }
    
}

</style>