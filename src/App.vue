<template>
  <div id="app">
    <AppHeader />
    <InformApp />
    <BehindeTariff />
    <CaseApp />
    <AppReview/>
    <FAq/>
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue';//
import InformApp from './components/InformApp.vue';//
import BehindeTariff from './components/BehindeTariff.vue';//
import FAq from "@/components/FAq.vue";//
import AppReview from "@/components/AppReview.vue";//
import CaseApp from "@/components/CaseApp.vue";
export default {
  components: {
    FAq,
    BehindeTariff,
    AppHeader,
    CaseApp,
    InformApp,
    AppReview,
  },
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap');

* {
  font-family: 'Montserrat', sans-serif;
}
</style>

