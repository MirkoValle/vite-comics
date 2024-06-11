<script>
export default{
    data() {
        return{
            
        }
    }
}
</script>

<template>
<div>
    <section class="container">
        <button>Sign-up now!</button>
        <div>
            <h2>follow us</h2>
            <img src="../assets/img/footer-facebook.png" alt="">
            <img src="../assets/img/footer-twitter.png" alt="">
            <img src="../assets/img/footer-youtube.png" alt="">
            <img src="../assets/img/footer-pinterest.png" alt="">
            <img src="../assets/img/footer-periscope.png" alt="">
        </div>
    </section>
</div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;


div{
    background-color: $dark-grey-color;
    section{
        @include container;
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 2rem;
        text-transform: uppercase;

        button{
            text-transform: uppercase;
            font-size: 1rem;
            color: white;
            background-color: transparent;
            border: .2rem solid $blue-color;
            padding: 1rem;
            font-weight: 500;
            cursor: pointer;
        }

        div{
            display: flex;
            justify-content: space-between;
            align-items: center;
            color: $blue-color;
            font-size: .8rem;

            img{
                padding-left: 1rem;
                cursor: pointer;
            }
        }

    }

}


</style>