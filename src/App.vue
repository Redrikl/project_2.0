<template>
  <div id="app">
    <AppHeader />
    <Inform />
    <Behinde />
    <Review/>
    <FAq/>
  </div>
</template>

<script>
import Header from './components/AppHeader.vue';//
import Inform from './components/Inform.vue';//
import Behinde from './components/Behinde.vue';//
import FAq from "@/components/FAq.vue";//
import Review from "@/components/Review.vue";//
export default {
  components: {
    FAq,
    Behinde,
    AppHeader,
    Inform,
    Review,
  },
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap');

* {
  font-family: 'Montserrat', sans-serif;
}
</style>

