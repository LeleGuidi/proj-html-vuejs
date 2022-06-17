<template>
    <div class="card" :style="'background-image: url('+items.path+')'">
        <div class="card_detail">
            <BaseSeparator class="separator" v-show="(items.separator == true)"/>
            <h3 v-show="(items.title)">{{items.title}}</h3>
            <span v-show="(items.subtitle)">{{items.subtitle}}</span>
        </div>
        <BasePlayButton v-show="(items.play_button == true)" class="play_button" :class="(items.play_button_size == 'medium') ? 'play_button_medium' : '' || (items.play_button_size == 'small') ? 'play_button_small' : '' "/>
    </div>
</template>

<script>
import BasePlayButton from '../smallCommons/BasePlayButton.vue'
import BaseSeparator from '../smallCommons/BaseSeparator.vue'
export default {
  components: { BaseSeparator, BasePlayButton },
    name: 'BaseCardBorderRadius',
    props: {
        items: Object,
    }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/_mixins.scss';
.card {
    // Per comodità il padding bottom (così da mantenere il ratio della card) va applicato a questo componente ma attraverso il padre 
    // Applicato stile alla card 
    border-radius: .1825rem;
    border-bottom-right-radius: 1.25rem;
    background-size: cover;
    // Applicato position relative per spostare il componente dei dettagli
    position: relative;

    &:hover {
        transform: scale(1.05);
    }
    &_detail{
        // Applicato position absolute, in modo da poter applicare un padding bottom alla card in modo da mantenere il ratio 
        position: absolute;
        bottom: 1.25rem;
        left: 1.25rem;
        .separator {
            color: var(--white);
            padding-bottom: 1rem;
        }
        h3 {
            color: var(--white);
        }
        span {
            color: var(--yellow);
        }
    }
.play_button {
    position: absolute;
    top: 45%;
    left: 45%;
    transform: translate(-50%, -50%);
}
.play_button_medium {
    transform: scale(0.7) translate(-50%, -50%);
}
.play_button_small {
    transform: scale(0.5) translate(-50%, -50%);
}
    

}
</style>