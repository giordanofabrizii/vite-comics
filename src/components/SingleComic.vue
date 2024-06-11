<script>
export default{
    data() {
        return{
            
        }
    },
    props: {
        singleCard: Object
    }
}
</script>

<template>
    <article>
        <img :src="singleCard.thumb" :alt="singleCard.series">
        <h3>{{ singleCard.series }}</h3>
    </article>
</template>

<style lang="scss" scoped>
    article{
        width: calc(100% / 6);
        padding: 1rem;

        &:hover img{
            animation: rotate .5s linear infinite;
        }

        img{
            width: 100%;
            aspect-ratio: 1/1;
            object-fit: cover;
            object-position: top;
        }

        h3 {
            text-transform: uppercase;
            font-size: 1rem;
            margin-top: 1rem;
        }
    }

    @keyframes rotate{
        0%{
            transform: rotate(0deg) scale(1);
        }
        50%{
            transform: rotate(180deg) scale(2)
        }
        100%{
            transform: rotate(360deg) scale(1);
        }
    }

</style>