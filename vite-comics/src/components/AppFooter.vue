<script>
export default{
    data() {
        return{
            footerLinks:[
                {
                    title: 'DC Comics',
                    links: [
                        {
                            name: 'Characters',
                            url: '',
                        },
                        {
                            name: 'Comics',
                            url: '',
                        },
                        {
                            name: 'Movies',
                            url: '',
                        },
                        {
                            name: 'TV',
                            url: '',
                        },
                        {
                            name: 'Games',
                            url: '',
                        },
                        {
                            name: 'Videos',
                            url: '',
                        },
                        {
                            name: 'News',
                            url: '',
                        },
                    ]
                },
                {
                    title: 'Shop',
                    links: [
                        {
                            name: 'Shop DC',
                            url: '',
                        },
                        {
                            name: 'Shop DC Collectibles',
                            url: '',
                        },
                    ]
                },
                {
                    title: 'DC',
                    links: [
                        {
                            name: 'Terms Of Use',
                            url: '',
                        },
                        {
                            name: 'Privacy policy(New)',
                            url: '',
                        },
                        {
                            name: 'Ad Choices',
                            url: '',
                        },
                        {
                            name: 'Advertising',
                            url: '',
                        },
                        {
                            name: 'Jobs',
                            url: '',
                        },
                        {
                            name: 'Subscriptions',
                            url: '',
                        },
                        {
                            name: 'Talent Workshops',
                            url: '',
                        },
                        {
                            name: 'CSPC Certificates',
                            url: '',
                        },
                        {
                            name: 'Ratings',
                            url: '',
                        },
                        {
                            name: 'Shop Help',
                            url: '',
                        },
                        {
                            name: 'Contact Us',
                            url: '',
                        },
                    ]
                },
                {
                    title: 'Sites',
                    links: [
                        {
                            name: 'DC',
                            url: '',
                        },
                        {
                            name: 'MAD Magazine',
                            url: '',
                        },
                        {
                            name: 'DC Kids',
                            url: '',
                        },
                        {
                            name: 'DC Universe',
                            url: '',
                        },
                        {
                            name: 'DC Power Visa',
                            url: '',
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
    <section>
        <div>
            <nav v-for="(link, index) in footerLinks" :key="index">
                <h2>
                {{ link.title }}
                </h2>
                <div>
                <a v-for="(link, index) in link.links" key="index" href="link.url">{{ link.name }}</a>
                </div>
            </nav>
        </div>
        <img src="../assets/img/dc-logo-bg.png" alt="">
    </section>
</div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

div.container{
    background-image: url(../assets/img/footer-bg.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    padding: 1rem;
    max-height: 21.3rem;
    overflow: hidden;
    section{
        @include container;
        display: flex;
        justify-content: space-between;
        div{
            display: flex;
            flex-direction: column;
            max-height: 20rem;
            width: 10rem;
            flex-wrap: wrap;
            justify-content: start;
            nav{
            display: flex;
            flex-direction: column;
            align-items: start;
                h2{
                    text-transform: uppercase;
                    color: white;
                    font-size: 1.2rem;
                }
                div{
                    display: flex;
                    flex-direction: column;
                    a{
                        color: $light-grey-color;
                        font-size: .8rem;
                        margin-bottom: .3rem;
                    }
                }
            }   
        }
        img{
            transform: translateY(-8rem);
        }
    }
}

</style>