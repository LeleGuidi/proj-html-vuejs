<template>
  <section class="articles">
    <div class="articles_container">
        <div class="articles_latest">
            <h4>Latest articles</h4>
            <a href="#/">Read all articles <i class="fa-solid fa-angle-right"></i></a>
        </div>
        <div class="bottom_row">
            <div v-for="(article, i) in articles" :key="i" class="col">
                <img :src="article.path" :alt="article.title">
                <div class="article_details">
                    <h5>{{article.article_title}}</h5>
                    <span>{{article.article_subtitle}}</span>
                </div>
            </div>
        </div>
    </div>
  </section>
</template>

<script>
export default {
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
            img {
                width: 100%;
            }
            h5 {
                padding-bottom: 0.3rem;
                font-weight: 400;
                font-size: 1rem
            }
            span {
                color: var(--silver);
                font-size: small;
            }
            h5, span {
                padding-left: 1rem;
            }
        }
    }
}

</style>