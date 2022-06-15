<template>
  <div class="footer_top">
    <div class="left_col">
        <img src="../../assets/img/logo small.png" alt="Avada Fitness Logo">
        <p>Ac aliquam neque sagittis diam faucibus vitae purus turpis phasellus. Pollentesque consectetur amet purus ultrices mauris.</p>
        <div class="socials">
            <i class="fa-brands fa-facebook-f"></i>
            <i class="fa-brands fa-twitter"></i>
            <i class="fa-brands fa-youtube"></i>
            <i class="fa-brands fa-instagram"></i>
            <i class="fa-brands fa-linkedin-in"></i>
        </div>
    </div>
    <div class="mid_col">
        <h4>Recent posts</h4>
        <FooterList/>
    </div>
    <div class="right_col">
        <h4>Contact informations</h4>
        <p>4746 Tipple Road Michigan 48449</p>
        <div class="contacts">
            <p>Mobile : 1.800.000.0000</p>
            <p>Email : info@your-company.com</p>
        </div>
    </div>
  </div>
</template>

<script>
import FooterList from '../commons/FooterList.vue'
export default {
  components: { FooterList },

}
</script>

<style lang="scss" scoped>
@import '../../assets/style/_mixins.scss';
.footer_top {
    // Attribuito al footer top display flex, larghezze, padding e text align 
    @include FlexRowBetween;
    align-items: start;
    gap: 2.75rem;
    text-align: center;
    @include MainContainer;
    padding: 6.25rem 0;
    color: var(--white);

    // Alle tre colonne attribuito il flex con direction column e le grandezze
    .left_col, .mid_col, .right_col {
        @include FlexColumnBetween;
        width: calc(100% / 3 - 0.91rem);
    }
    h4 {
        text-transform: uppercase;
    }
    p {
        color: var(--silver)
    }

    .left_col {
        gap: 2.3rem;
        img {
            width: 12rem;
        }
        .socials {
        @include FlexRowBetween;
        gap: 0.8rem;
        color: var(--burnt-sienna);
        }
    }
    .mid_col, .right_col {
        gap: 1.3rem;
    }
    .right_col {
        .contacts {
        font-weight: bold;
        p{
            color: var(--white);
        }
    }
    }
}

</style>