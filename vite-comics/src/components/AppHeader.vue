<script>
export default{
    data() {
        return{
            headerLinks: [
                {
                    name: 'characters',
                    url: '',
                    active: 'none'
                },
                {
                    name: 'comics',
                    url: '',
                    active: 'none'
                },
                {
                    name: 'movies',
                    url: '',
                    active: 'none'
                },
                {
                    name: 'tv',
                    url: '',
                    active: 'none'
                },
                {
                    name: 'games',
                    url: '',
                    active: 'none'
                },
                {
                    name: 'collectibles',
                    url: '',
                    active: 'none'
                },
                {
                    name: 'videos',
                    url: '',
                    active: 'none'
                },
                {
                    name: 'fans',
                    url: '',
                    active: 'none'
                },
                {
                    name: 'news',
                    url: '',
                    active: 'none'  
                },
                {
                    name: 'shop',
                    url: '',
                    active: 'false'
                },
            ],
            activeLink: 0,
        }
    },
    methods:{
        changeIndex:function(index){
            this.activeLink = index;
            this.changeActive()
        },

        changeActive: function(){
            this.headerLinks.forEach((link, index) => {
                if (index == this.activeLink) {
                    link.active = 'true';
                } else {
                    link.active = 'false'
                }
            });
        }
    },
}
</script>

<template>
<section>
    <div><img src="../assets/img/dc-logo.png" alt="Main logo DC"></div>
    <nav>
        <ul>
            <li v-for="(link, index) in headerLinks" :key="index" :class="(link.active == 'true') ? 'active' : ''" @click="changeIndex(index)">
                    {{ link.name }}
            </li>
        </ul>
    </nav>

</section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

section{
    display: flex;
    justify-content: space-between;
    align-items: center;
    @include container;
    img{
        width: 5rem;
    }
    ul{
        display: flex;
        margin: 0;
        li{
            cursor: pointer;
                padding: 3rem 0;
                margin: 0 1rem;
                text-transform: uppercase;
                font-size: .8rem;
                font-weight: 600;
                color: $dark-grey-color;
                border-bottom: .5rem solid transparent;

                &.active{
                            border-bottom: .5rem solid $blue-color;
                            color: $blue-color;
                        }
        }
    }
}
</style>