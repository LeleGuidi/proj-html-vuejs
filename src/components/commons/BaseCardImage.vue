<template>
  <div class="card">
    <img :src="items.path" :alt="items.title">
    <div class="article_details">
        <h5>{{items.article_title}}</h5>
        <span>{{items.article_subtitle}}</span>
    </div>
  </div>
</template>

<script>
export default {
    name: 'BaseCardImage',
    props: {
        items: Object,
    }
}
</script>

<style lang="scss" scoped>
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
</style>