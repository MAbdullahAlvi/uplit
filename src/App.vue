<template>
  <div id="app">
    <router-view></router-view>
    <TheCarousel v-if="isHomePage" />
    <EntertainmentFuture v-if="isHomePage" />
    <Sec3Component v-if="isHomePage" />
    <FeatureGrid v-if="isHomePage" />
    <PastExperiences v-if="isHomePage" />
    <Partnerships v-if="isHomePage" />
    <MainSection v-if="isHomePage" />
    <FooterSection v-if="isHomePage" />
  </div>
</template>

<script>
//import { mapState } from 'vuex';
import TheCarousel from './components/TheCarousel.vue';
import EntertainmentFuture from './components/EntertainmentFuture.vue';
import Sec3Component from './components/Sec3Component.vue';
import FeatureGrid from './components/FeatureGrid.vue';
import PastExperiences from './components/PastExperiences.vue';
import Partnerships from './components/Partnerships.vue';
import MainSection from './components/MainSection.vue';
import FooterSection from './components/FooterSection.vue';

export default {
  name: 'App',
  components: {
    EntertainmentFuture,
    Sec3Component,
    FeatureGrid,
    PastExperiences,
    Partnerships,
    MainSection,
    FooterSection,
    TheCarousel,
  },
  computed: {
    isHomePage() {
      return this.$route.path === '/';
    }
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
@media (max-width: 768px) {
  .features {
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  }
}
</style>
