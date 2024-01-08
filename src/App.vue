<template>
  <div id="app">
    <AppHeader />
    <InformApp />
    <SupportApp />
    <TarifApp />
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
import SupportApp from './components/SupportApp.vue';
import TarifApp from "./components/TarifApp.vue";

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
    SupportApp,
    TarifApp,
  },
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap');

* {
  font-family: 'Montserrat', sans-serif;
}
</style>
