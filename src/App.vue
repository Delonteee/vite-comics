<script>

import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppBlueSection from './components/AppBlueSection.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  data() {
    return {

    };
  },
  components: {
    AppHeader,
    AppMain,
    AppBlueSection,
    AppFooter,
  },
  methods: {

  }
}
</script>

<template>
  
  <AppHeader />

  <AppMain />

  <AppBlueSection />

  <AppFooter />

</template>

<style lang="scss">

@use "assets/scss/main.scss" as *;
@import "assets/scss/partials/reset.scss";
@import url('https://fonts.googleapis.com/css2?family=Fredoka:wght@400;700&family=Oswald:wght@200;400;700&display=swap');


</style>
