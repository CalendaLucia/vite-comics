<script>
import AppHeader from './components/Appheader.vue'
import AppMain from './components/AppMain.vue'
import AppFooter from './components/AppFooter.vue'
import AppCards from './components/AppCards.vue'
import comicData from './comicData.json';


export default {
  components: {
    AppHeader,
    AppFooter,
    AppMain,
},
  data() {
    return {
      comicData
    };
  }
};
</script>

<template>
  <AppHeader/>
  <AppCards :comics="comicData" />
  <AppMain/>
  <AppFooter/>

</template>

<style lang="scss">
</style>
