<template>
  <section class="articles">
    <div class="articles_container">
        <BaseTitleRow title="Latest articles" link="Read all articles"/>
        <div class="bottom_row">
            <BaseCardImage v-for="(article, i) in articles" :key="i" class="col" :items="article"/>
        </div>
    </div>
  </section>
</template>

<script>
import BaseCardImage from '../commons/BaseCardImage.vue'
import BaseTitleRow from '../commons/BaseTitleRow.vue'
export default {
  components: { BaseCardImage, BaseTitleRow },
    name: 'SectionArticles',
    data() {
        return {
            articles: [
                {
                    path: require('../../assets/img/blog4-2x-400x258.jpg'),
                    article_title: 'The best protein shake',
                    article_subtitle: 'By adim | November 26th, 2019 | Gym',
                },
                {
                    path: require('../../assets/img/blog1-2x-400x258.jpg'),
                    article_title: 'Ultimate cardio workout',
                    article_subtitle: 'By adim | November 26th, 2019 | Gym',
                },
                {
                    path: require('../../assets/img/blog3-2x-400x258.jpg'),
                    article_title: 'New juices available now',
                    article_subtitle: 'By adim | November 26th, 2019 | Gym',
                },
            ]
        }
    }
}
</script>

<style lang="scss">
@import '../../assets/style/_mixins.scss';
.articles {
    width: 100%;
    padding: 6rem 0;
    &_container {
        @include MainContainer;

        .articles_latest {
            @include FlexRowBetween;
            padding: 0 0 2rem 0;

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
            gap: 3rem;

            .col {
                width: calc(100% / 3);
                @include FlexColumnBetween;
                align-items: flex-start;
                gap: 1.5rem;
            }
        }
    }
}

</style>