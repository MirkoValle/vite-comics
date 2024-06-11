<script>
export default{
    data() {
        return{
            blueLinks:[
                {
                    name: 'digital comics',
                    url: '',
                    src: 'buy-comics-digital-comics.png',
                },
                {
                    name: 'dc merchandise',
                    url: '',
                    src: 'buy-comics-merchandise.png',
                },
                {
                    name: 'subscription',
                    url: '',
                    src: 'buy-comics-subscriptions.png'
                },
                {
                    name: 'comic shop locator',
                    url: '',
                    src: 'buy-comics-shop-locator.png'
                },
                {
                    name: 'dc power visa',
                    url: '',
                    src: 'buy-dc-power-visa.svg'
                },
            ],
        }
    }
}
</script>

<template>
    <div class="container">
        <section>
            <ul>
                <li v-for="(link, index) in blueLinks" :key="index">
                    <a href="link.url"></a>
                    <img :src="'../src/assets/img/' + link.src" alt="">
                    <h2>{{ link.name }}</h2>
                </li>
            </ul>
        </section>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;


.container{
    background-color: $blue-color;
    padding: 2rem;
    section{
        @include container;
        ul{
            display: flex;
            justify-content: space-between;

            li{
                display: flex;
                align-items: center;
                text-transform: uppercase;
                padding: 1rem;
                width: calc((100% / 5) );
                cursor: pointer;

                &:hover{
                    background-color: rgba(231, 231, 231, 0.164);
                }

                img{
                    width: 3rem;
                }
                h2{
                    padding-left: 1rem;
                    font-size: 1rem;
                    color: white;
                }
            }
        }
    } 
}
</style>