<template>
  <div class="navbar">
    <ul class="navbar_list">
        <li v-for="(item, i) in navbarItems" :key="i"><a :class="(i == 0)? 'active' : ''" href="#/">{{item}}</a></li>
    </ul>
  </div>
</template>

<script>
export default {
    name: 'BaseNavbar',
    data() {
        return {
            navbarItems: ['Home', 'Services', 'About', 'Videos', 'Blog', 'Store'],
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/_mixins.scss';
.navbar {
    color: var(--jumbo);

    &_list {
        // Stile alla lista, colori e display flex 
        list-style: none;
        @include FlexRowBetween;
        gap: 1.5rem;

        // Aggiunta del contenuto "new" all'ultimo item della lista 
        li:last-child::after {
            content: 'new';
            margin: 0 0.5rem;
            padding: 0.2rem 0.3rem;
            display: inline-block;
            background-color: var(--yellow);
            font-size: 0.8rem;
            border-radius: .1875rem;

        }

        // stili al tag a della lista 
        a {
            text-decoration: none;
            color: inherit;
        }

        // Stile al tag active, attribuito al tag a attivato 
        .active {
            color: white;
        }
    }
}
</style>