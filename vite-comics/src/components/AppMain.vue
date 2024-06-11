<script>
import AppBottomMain from "./AppBottomMain.vue";

export default{
    components:{
    AppBottomMain,
},
    data() {
        return{
            
        }
    }
}
</script>

<template>
    <div class="jumbo">
        
    </div>
<div class="container">
    <section>
        <h1> --> Content goes here <-- </h1>
    </section>
</div>
<AppBottomMain/>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;


div.jumbo{
    background-image: url(../assets/img/jumbotron.jpg);
    height: 19rem;
}
div{
    background-color: $dark;
    padding: 3rem;
    section{
        @include container;
        h1{
        color: white;
        margin: 0;
    } 
    }
}

</style>