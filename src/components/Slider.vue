<script>
import Swiper from 'swiper';
import 'swiper/swiper-bundle.css';
import Partner from "@/components/Partner.vue";
import pic1 from "../assets/img/logo.png";
import pic2 from "../assets/img/logo_0.png";
import pic3 from "../assets/img/logo_2.png";
import pic4 from "../assets/img/11.jpg";
import pic5 from "../assets/img/nashagazeta_ch.png";
import pic6 from "../assets/img/1.jpg";
import pic7 from "../assets/img/2.jpg"
import pic8 from "../assets/img/3.webp"
import pic9 from "../assets/img/4.png"
import pic10 from "../assets/img/10.png"
import pic11 from "../assets/img/11.jpg"
import pic12 from "../assets/img/12.jpg"
import pic13 from "../assets/img/dodo.jpg"
import pic14 from "../assets/img/kfc.png"
import pic15 from "../assets/img/mac.png"
import pic16 from "../assets/img/9.jpg"
import pic17 from "../assets/img/5.jpg"
import pic18 from "../assets/img/6.jpg"
import pic19 from "../assets/img/7.jpg"
import pic20 from "../assets/img/8.png"
import pic21 from "../assets/img/logo.png";
import pic22 from "../assets/img/logo_0.png";
import pic23 from "../assets/img/logo_2.png";
import pic24 from "../assets/img/12.jpg";


export default {
  name: "WorkWithUs",
  components: {Partner},
  data: () => {
    return {
      pic1, pic2, pic3, pic4,
      pic5, pic6, pic7, pic8,
      pic9, pic10, pic11, pic12,
      pic13, pic14, pic15, pic16,
      pic17, pic18, pic19, pic20,
      pic21, pic22,pic23,pic24
    }
  },
  mounted() {
    const swiper1 = new Swiper(this.$refs.swiper1, {
      slidesPerView: 'auto',
      spaceBetween: 5,
      centeredSlides: true,
      loop: true,
      longSwipes: false,
    });

    const swiper2 = new Swiper(this.$refs.swiper2, {
      slidesPerView: 'auto',
      spaceBetween: 5,
      centeredSlides: false,
      loop: true,
      longSwipes: false,
    });
    setInterval(() => {
      swiper1.slideNext();
      swiper2.slideNext();
    }, 3000);
  },
}
</script>

<template>
  <div class="work-main-block">
    <div class="container-fluid wind">
      <div class="row justify-content-center">
        <div class="col-12">
          <h1 class="wwu-title">
            С нами работают
          </h1>
          <div class="wwu-text col-8 mx-auto">
            Десятки компаний доверяют нам самок ценное, что у них есть в интернете -
            свои сайты. Мы делаем всё, чтобы наше сотрудничество было долгим.
          </div>
        </div>
      </div>
      <div class="swiper-container" ref="swiper1">
        <div class="swiper-wrapper">
          <div class="swiper-slide">
            <Partner :image="pic1"/>
          </div>
          <div class="swiper-slide">
            <Partner :image="pic13"/>
          </div>
          <div class="swiper-slide">
            <Partner :image="pic17"/>
          </div>
          <div class="swiper-slide">
            <Partner :image="pic19"/>
          </div>
          <div class="swiper-slide">
            <Partner :image="pic3"/>
          </div>
          <div class="swiper-slide">
            <Partner :image="pic7"/>
          </div>
          <div class="swiper-slide">
            <Partner :image="pic15"/>
          </div>
          <div class="swiper-slide">
            <Partner :image="pic12"/>
          </div>
          <div class="swiper-slide">
            <Partner :image="pic20"/>
          </div>
          <div class="swiper-slide">
            <Partner :image="pic4"/>
          </div>
          <div class="swiper-slide">
            <Partner :image="pic10"/>
          </div>
          <div class="swiper-slide">
            <Partner :image="pic8"/>
          </div>
          <div class="swiper-slide">
            <Partner :image="pic14"/>
          </div>
          <div class="swiper-slide">
            <Partner :image="pic2"/>
          </div>
          <div class="swiper-slide">
            <Partner :image="pic11"/>
          </div>
          <div class="swiper-slide">
            <Partner :image="pic16"/>
          </div>
          <div class="swiper-slide">
            <Partner :image="pic18"/>
          </div>
          <div class="swiper-slide">
            <Partner :image="pic21"/>
          </div>
          <div class="swiper-slide">
            <Partner :image="pic22"/>
          </div>
          <div class="swiper-slide">
            <Partner :image="pic13"/>
          </div>
          <div class="swiper-slide">
            <Partner :image="pic24"/>
          </div>
        </div>

      </div>
      <div class="swiper-container" ref="swiper2">
        <div class="swiper-wrapper swipe2">
          <div class="swiper-slide">
            <Partner :image="pic4"/>
          </div>
          <div class="swiper-slide">
            <Partner :image="pic5"/>
          </div>
          <div class="swiper-slide">
            <Partner :image="pic6"/>
          </div>
          <div class="swiper-slide">
            <Partner :image="pic12"/>
          </div>
          <div class="swiper-slide">
            <Partner :image="pic20"/>
          </div>
          <div class="swiper-slide">
            <Partner :image="pic8"/>
          </div>
          <div class="swiper-slide">
            <Partner :image="pic16"/>
          </div>
          <div class="swiper-slide">
            <Partner :image="pic7"/>
          </div>
          <div class="swiper-slide">
            <Partner :image="pic14"/>
          </div>
          <div class="swiper-slide">
            <Partner :image="pic18"/>
          </div>
          <div class="swiper-slide">
            <Partner :image="pic10"/>
          </div>
          <div class="swiper-slide">
            <Partner :image="pic11"/>
          </div>
          <div class="swiper-slide">
            <Partner :image="pic19"/>
          </div>
          <div class="swiper-slide">
            <Partner :image="pic17"/>
          </div>
          <div class="swiper-slide">
            <Partner :image="pic13"/>
          </div>
          <div class="swiper-slide">
            <Partner :image="pic9"/>
          </div>
          <div class="swiper-slide">
            <Partner :image="pic3"/>
          </div>
          <div class="swiper-slide">
            <Partner :image="pic21"/>
          </div>
          <div class="swiper-slide">
            <Partner :image="pic22"/>
          </div>
          <div class="swiper-slide">
            <Partner :image="pic13"/>
          </div>
          <div class="swiper-slide">
            <Partner :image="pic24"/>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.wind {
  max-width: 100%;
  overflow: hidden;
}


.swiper-slide {
  margin: 5px;
  width: 160px;
  height: 90px;
  float: left;
}

.work-main-block {
  position: relative;
}

.wwu-title {
  padding-top: 100px;
  margin-bottom: 20px;
  text-align: center;
  color: #050c33;
  font-weight: 700;
  font-size: 42px;
}

.wwu-text {
  text-align: center;
  margin-bottom: 40px;
}

@media screen and (min-width: 768px) {
  .wwu-title {
    margin-bottom: 55px;
    font-size: 42px;
  }

  .swiper-slide {
    width: 225px;
    height: 115px;
  }


}
</style>
