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
        <section>
            <h1>prova</h1>
        </section>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;


.container{
    background-color: $blue-color;
    padding: 3rem;
    section{
        @include container;
        h1{
            color: white;
        }
    } 
}
</style>