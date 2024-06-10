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
        <section>
            
        </section>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;


div{
    background-color: $blue-color;
    padding: 3rem;
    section{
        @include container;
    } 
}
</style>