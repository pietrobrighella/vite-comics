<template>
  <HeaderComponent/>
  <MainComponent/>
  <SubMainComponent/>
  <FooterComponent />
  <SubFooterComponent/>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import MainComponent from './components/MainComponent.vue';
import SubMainComponent from './components/SubMainComponent.vue';
import FooterComponent from './components/FooterComponent.vue';
import SubFooterComponent from './components/SubFooterComponent.vue';

  export default {
    components: { HeaderComponent, MainComponent, SubMainComponent, FooterComponent, SubFooterComponent }
}
</script>

<style lang="scss">

</style>