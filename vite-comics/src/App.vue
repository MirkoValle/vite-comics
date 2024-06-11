<script>
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";
import AppFooter from "./components/AppFooter.vue";
import BottomSocials from "./components/BottomSocials.vue";

  export default{
    components:{
      AppHeader,
      AppMain,
      AppFooter,
      BottomSocials,
    }
  }
</script>

<template>
    <AppHeader/>
    <AppMain/>
    <AppFooter/>
    <BottomSocials/>
</template>

<style lang="scss">
@use './styles/general.scss';
@use './styles/partials/variables' as *;
</style>