<script>
export default{
    data() {
        return{
            headerLinks: [
                {
                    name: 'characters',
                    link: 'www.google.com',
                    active: 'none'
                },
                {
                    name: 'comics',
                    link: 'www.google.com',
                    active: 'none'
                },
                {
                    name: 'movies',
                    link: 'www.google.com',
                    active: 'none'
                },
                {
                    name: 'tv',
                    link: 'www.google.com',
                    active: 'none'
                },
                {
                    name: 'games',
                    link: 'www.google.com',
                    active: 'none'
                },
                {
                    name: 'collectibles',
                    link: 'www.google.com',
                    active: 'none'
                },
                {
                    name: 'videos',
                    link: 'www.google.com',
                    active: 'none'
                },
                {
                    name: 'fans',
                    link: 'www.google.com',
                    active: 'none'
                },
                {
                    name: 'news',
                    link: 'www.google.com',
                    active: 'none'  
                },
                {
                    name: 'shop',
                    link: 'www.google.com',
                    active: 'none'
                },
            ],
        }
    },
    methods:{
        open: function(i){
            this.headerLinks.forEach((link, index) => {
                if (index == i) {
                    link.active = 'true';
                } else {
                    link.active = 'none'
                }
            });
        }
    },
    mounted(){
        this.open(1)
    }
}
</script>

<template>
    <div class="container">
        <img src="../assets/img/dc-logo.png" alt="DC logo">
        <ul>
            <li v-for="(item, index) in headerLinks" :key="index" :class="(item.active == 'true') ? 'active' : ''" @click="open(index)">
                {{ item.name }}
            </li>
        </ul>
    </div>
</template>

<style lang="scss" scoped>
    @use '../styles/partials/variables.scss' as *;
    @use '../styles/partials/mixins.scss' as *;
    @use '../styles/general';
    .container{
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

                &.active{
                    border-bottom: .5rem solid $primary;

                }
            }
        }
    }
</style>