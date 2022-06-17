<template>
  <div class="card">
    <div class="img">
        <img :src="items.path" :alt="items.title">
        <div class="effect_hover"></div>
    </div>
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
.card {

}
.img {
    font-size: 0;
    position: relative;
}
.img:hover .effect_hover{
    background: linear-gradient(0deg, rgba(67,33,170,0.7) 0%, rgba(0,0,0,0) 60%);
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
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
</style>