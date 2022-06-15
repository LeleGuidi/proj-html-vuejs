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
        list-style: none;
        @include FlexRowBetween;
        gap: 2rem;

        li:last-child::after {
            content: 'new';
            margin: 0 0.8rem;
            padding: 0.2rem 0.4rem;
            display: inline-block;
            background-color: #fff941;
            font-size: 0.8rem;
            border-radius: .1875rem;

        }

        a {
            text-decoration: none;
            color: inherit;
        }

        .active {
            color: white;
        }
    }
}
</style>