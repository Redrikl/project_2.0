<template>
  <div id="app">
    <AppHeader />
    <InformApp />
    <BehindeTariff />
    <TeamApp />
    <Slider />
    <CaseApp />
    <AppReview/>
    <FAq/>
    <FooterApp />
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue';
import InformApp from './components/InformApp.vue';
import BehindeTariff from './components/BehindeTariff.vue';
import Slider from './components/Slider.vue';
import CaseApp from "@/components/CaseApp.vue";
import FooterApp from "@/components/FooterApp.vue";
import FAq from "@/components/FAq.vue";
import AppReview from "@/components/AppReview.vue";
import TeamApp from './components/TeamApp.vue';

export default {
  components: {
    FAq,
    TeamApp,
    BehindeTariff,
    Slider,
    AppHeader,
    InformApp,
    CaseApp,
    AppReview,
    FooterApp,
  },
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap');

* {
  font-family: 'Montserrat', sans-serif;
}
</style>
