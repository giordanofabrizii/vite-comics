<script>
export default{
    data() {
        return{
            headerLinks: [
                {
                    name: 'characters',
                    link: 'www.google.com',
                },
                {
                    name: 'comics',
                    link: 'www.google.com',
                },
                {
                    name: 'movies',
                    link: 'www.google.com',
                },
                {
                    name: 'tv',
                    link: 'www.google.com',
                },
                {
                    name: 'games',
                    link: 'www.google.com',
                },
                {
                    name: 'collectibles',
                    link: 'www.google.com',
                },
                {
                    name: 'videos',
                    link: 'www.google.com',
                },
                {
                    name: 'fans',
                    link: 'www.google.com',
                },
                {
                    name: 'news',
                    link: 'www.google.com',
                },
                {
                    name: 'shop',
                    link: 'www.google.com',
                },
            ],
        }
    }
}
</script>

<template>
    <header class="container">
        <img src="../assets/img/dc-logo.png" alt="DC logo">
        <ul>
            <li v-for="(item, index) in headerLinks" :key="index">
                <a :href="item.link">{{ item.name }}</a>
            </li>
        </ul>
    </header>
</template>

<style lang="scss" scoped>
    @use '../styles/partials/variables.scss' as *;
    @use '../styles/partials/mixins.scss' as *;
    @use '../styles/general';
    header{
        display: flex;
        justify-content: space-between;

        img{
            object-fit: contain
        }

        ul {
            @include flexRow;

            li {
                padding: 3rem 0;
                margin: 0 2rem;
                border-top: .5rem solid transparent;
                border-bottom: .5rem solid transparent;
                text-transform: uppercase;

                &:hover{
                    border-bottom: .5rem solid $primary;

                }
            }
        }
    }
</style>