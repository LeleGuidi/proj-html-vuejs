<template>
  <ul class="footer_list">
    <li v-for="(post, i) in recentPosts" :key="i"><i class="arrow fa-solid fa-chevron-right"></i> {{post}}</li>
  </ul>
</template>

<script>
export default {
    name: 'FooterList',
    data() {
        return {
            recentPosts: ['The best protein shake', 'Ultimate cardio workout', 'New juices available now', 'Tips to find training partners', '20 best healthy recipes']
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/_mixins.scss';
.footer_list {
    // Stile alla lista, colori e display flex 
    color: var(--white);
    list-style: none;
    @include FlexColumnBetween;
    gap: 0.9rem;

    li {
        // Flex per allineare l'icona al testa 
        @include FlexRowBetween;
        gap: 0.2rem;
    }
    .arrow {
        // ridurre il font all'icona 
        font-size: 0.7rem;
        
    }
}
</style>