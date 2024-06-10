<script>
export default{
    data() {
        return{
            
        }
    }
}
</script>

<template>
    <div class="container">
        <a href="" class="btn">Sign-up now!</a>
        <div class="link-container">
            <h2>Follow us</h2>
            <img src="../assets/img/footer-facebook.png" alt="facebook logo">
            <img src="../assets/img/footer-twitter.png" alt="twitter logo">
            <img src="../assets/img/footer-youtube.png" alt="youtube logo">
            <img src="../assets/img/footer-pinterest.png" alt="pinterest logo">
            <img src="../assets/img/footer-periscope.png" alt="periscope logo">
        </div>
    </div>
</template>

<style lang="scss" scoped>
    @use '../styles/general.scss';
    @use '../styles/partials/mixins.scss' as *;
    @use '../styles/partials/variables.scss' as *;

    .container {
        @include flexRow;
        justify-content: space-between;
        padding: 2.5rem 0;

        .btn {
            border: 3px solid $primary;
            color: white;
            padding: 1rem;
            text-transform: uppercase;
            font-weight: 600;
            font-size: 1.3rem;
            background: linear-gradient(to left, $quaternary 50%, white 50%);
            background-size: 300% 100%;
            background-position: right bottom;
            transition: all .5s linear;

            &:hover{
                background-position: left bottom;
                color: $secondary
            }
        }

        .link-container {
            @include flexRow;

            h2 {
                color: $primary;
                text-transform: uppercase;
                margin-right: 1rem;
                font-size: 1.7rem;
            }

            img {
                height: 2.7rem;
                margin: 0 1rem;

                &:hover{
                    height: 3rem;
                    margin: 0 .85rem;
                }
            }
        }
    }
</style>