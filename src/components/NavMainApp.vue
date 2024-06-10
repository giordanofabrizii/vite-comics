<script>
export default{
    data() {
        return{
            navLinks:[
                {
                    name: 'digital comics',
                    url: 'www.google.com',
                    src: 'buy-comics-digital-comics.png',
                },
                {
                    name: 'dc merchandise',
                    url: 'www.google.com',
                    src: 'buy-comics-merchandise.png',
                },
                {
                    name: 'subscription',
                    url: 'www.google.com',
                    src: 'buy-comics-subscriptions.png'
                },
                {
                    name: 'comic shop locator',
                    url: 'www.google.com',
                    src: 'buy-comics-shop-locator.png'
                },
                {
                    name: 'dc power visa',
                    url: 'www.google.com',
                    src: 'buy-dc-power-visa.svg'
                },
            ],
        }
    }
}
</script>

<template>
    <div class="container">
        <ul>
            <li v-for="(link,index) in navLinks" :key="index">
                <a :href="link.url">
                    <img :src="'./src//assets/img/' + link.src" alt="">
                    <h2>{{ link.name }}</h2>
                </a>
            </li>
        </ul>
    </div>
</template>

<style lang="scss" scoped>
    @use '../styles/partials/mixins.scss' as *;

    ul {
        @include flexRow;
        justify-content: space-between;

        li{
            text-transform: uppercase;
            padding: 2rem;
            width: calc(100% / 5);
            
            a{
                @include flexRow;

                img {
                    height: 5rem;
                }

                h2 {
                    font-size: 1rem;
                    margin: 0 1rem;
                    color: white;
                }
            }

            &:hover{
                background-color: rgba(255,255,255,0.4);
            }
        }
    }
</style>