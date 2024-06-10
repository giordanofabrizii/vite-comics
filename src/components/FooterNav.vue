<script>
export default{
    data() {
        return{
            footerLinks:[
                {
                    name: 'DC Comics',
                    links: [
                        {
                            title: 'Characters',
                            url: 'google.com',
                        },
                        {
                            title: 'Comics',
                            url: 'google.com',
                        },
                        {
                            title: 'Movies',
                            url: 'google.com',
                        },
                        {
                            title: 'TV',
                            url: 'google.com',
                        },
                        {
                            title: 'Games',
                            url: 'google.com',
                        },
                        {
                            title: 'Videos',
                            url: 'google.com',
                        },
                        {
                            title: 'News',
                            url: 'google.com',
                        },
                    ]
                },
                {
                    name: 'Shop',
                    links: [
                        {
                            title: 'Shop DC',
                            url: 'google.com',
                        },
                        {
                            title: 'Shop DC Collectibles',
                            url: 'google.com',
                        },
                    ]
                },
                {
                    name: 'DC',
                    links: [
                        {
                            title: 'Terms Of Use',
                            url: 'google.com',
                        },
                        {
                            title: 'Privacy policy(New)',
                            url: 'google.com',
                        },
                        {
                            title: 'Ad Choices',
                            url: 'google.com',
                        },
                        {
                            title: 'Advertising',
                            url: 'google.com',
                        },
                        {
                            title: 'Jobs',
                            url: 'google.com',
                        },
                        {
                            title: 'Subscriptions',
                            url: 'google.com',
                        },
                        {
                            title: 'Talent Workshops',
                            url: 'google.com',
                        },
                        {
                            title: 'CSPC Certificates',
                            url: 'google.com',
                        },
                        {
                            title: 'Ratings',
                            url: 'google.com',
                        },
                        {
                            title: 'Shop Help',
                            url: 'google.com',
                        },
                        {
                            title: 'Contact Us',
                            url: 'google.com',
                        },
                    ]
                },
                {
                    name: 'Shop',
                    links: [
                        {
                            title: 'DC',
                            url: 'google.com',
                        },
                        {
                            title: 'MAD Magazine',
                            url: 'google.com',
                        },
                        {
                            title: 'DC Kids',
                            url: 'google.com',
                        },
                        {
                            title: 'DC Universe',
                            url: 'google.com',
                        },
                        {
                            title: 'DC Power Visa',
                            url: 'google.com',
                        },
                    ]
                },
            ],
        }
    }
}
</script>

<template>
    <div class="container">
        <div id="nav-section">
            <nav v-for="(section, index) in footerLinks" :key="index">
                <h2>{{ section.name }}</h2>
                <div class="link-container">
                    <a v-for="(link, i) in section.links" :key="i" :href="link.url">{{ link.title }}</a>
                </div>
            </nav>
        </div>
        <img src="../assets/img/dc-logo-bg.png" alt="">
    </div>
</template>

<style lang="scss" scoped>
    @use '../styles/general.scss';
    @use '../styles/partials/mixins.scss' as *;
    @use '../styles/partials/variables.scss' as *;

    .container{
        @include flexRow;
        justify-content: space-between;
        max-height: 35rem;
        overflow: hidden;

        #nav-section{
            @include flexColumn;
            max-height: 30rem;
            width: 30rem;
            flex-wrap: wrap;
            justify-content: start;

            nav{
                @include flexColumn;
                align-items: start;
                width: 13rem;

                h2{
                    text-transform: uppercase;
                    margin: 1rem 0;
                    color: white;
                    text-align: start;
                }

                .link-container{
                    @include flexColumn;
                    align-items: start;
                    margin: .5rem 0;

                    a{
                        text-align: start;
                        font-size: 1.2rem;
                        color: $tertiary;
                        margin: .2rem 0;
                    }
                }

            }
        }

        img{
            height: 50rem;
        }
    }

</style>