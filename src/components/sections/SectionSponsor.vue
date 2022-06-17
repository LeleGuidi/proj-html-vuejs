<template>
    <section class="sponsor">
        <div class="sponsor_container">
            <div class="row">
                <BaseCardTextCenter v-for="(sponsor, i) in sponsors" :key="i" :items="sponsor" class="col"/>
            </div>
        </div>
    </section>
</template>

<script>
import BaseCardTextCenter from '../commons/BaseCardTextCenter.vue'
export default {
    components: { BaseCardTextCenter },
    name: 'SectionSponsor',
    data() {
        return {
            sponsors: [
                {
                    path: require('../../assets/img/sponsor-1-2x.png'),
                    details: 'Tristique aliquam in nullam habitasse nunc, amet vel consectetur. Nulla in suspendisse dolor, aliquet.',
                    link: 'Visit Yoga Studio',
                    separator: true,
                },
                {
                    path: require('../../assets/img/sponsor-2-2x.png'),
                    details: 'Feugiat etiam dui mauris pharetra mauris sed pharetra. Convallis sapien ornare cras faucibus nulla porta dui a.',
                    link: 'Join Fitness Center',
                    separator: true,
                },
                {
                    path: require('../../assets/img/sponsor-3-2x.png'),
                    details: 'Nisl at quam adipiscing montes, nec, adipiscing commodo aliquam tincidunt. Ligula in habitant et saggitis imperdiet.',
                    link: 'Learn about FC',
                    separator: true,
                },
                {
                    path: require('../../assets/img/sponsor-4-2x.png'),
                    details: 'Proin in viverra maecenas et mattis ut nibh. Gravida ultricies mi porta lacus. Et posuere velit sed nec eleifend.',
                    link: 'Visit Power Gym',
                    separator: true,
                },
            ]
        }
    }
}
</script>

<style lang="scss">
@import '../../assets/style/_mixins.scss';
.sponsor {
    &_container {
        @include MainContainer;

        .row {
            @include FlexRowBetween;
            align-items: stretch;
            gap: 2rem;
        }
        .col {
            width: calc(100% / 4 - .5rem);
            background-color: var(--white);
            border: 0;
            justify-content: center;
            gap: 1rem;
            padding: 0;

            .link {
                color: var(--jumbo);
                font-size: small;
                font-weight: 400;
            }
            .details {
                font-size: small;
                font-weight: 400;
            }
        }
    }
}
</style>