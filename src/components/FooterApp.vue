<template>
  <div class="container-fluid pt-5 pb-5 pb-md-0 footer-region" id="footerRegion">
    <div class="footer-region-background"></div>
    <div class="row d-flex">
      <div class="col-11 col-md-10 mx-auto px-0">
        <div class="row">
          <div class="col-11 col-md-5 mx-auto">
            <h5 class="text-head-footer text-md-start text-center">
              Оставить заявку на
              <br/>
              поддержку сайта
            </h5>
            <p class="text-extra-footer text-start">
              Срочно нужна поддержка сайта? Ваша команда не успевает справиться самостоятельно или предыдущий подрядчик
              не справился с работой?
              Тогда вам точно к нам! Просто оставьте заявку и наш менеджер с вами свяжется!
            </p>
            <div class="text-start phone">
              <img src="../assets/img/phoneicon.png" alt="">
              <a class="text-light text-decoration-none phone" href="tel:88002222673">
                8 800 222-26-73
              </a>
            </div>
            <div class="text-start email">
              <img src="../assets/img/mail.png" alt="">
              <a class="text-light email" href="mailto:info@drupal-coder.ru">

                info@drupal-coder.ru
              </a>
            </div>
          </div>
          <div class="col-11 col-md-5 mx-auto">
            <AppForm/>
          </div>

          <div class="col-12 footer-social">
            <div class="row">
              <div class="col-md-6 col-12">
                <div class="row">
                  <div class="social-block">
                    <ul class="social-list">
                      <li class="social-list-item">
                        <a href="#"
                        ><img src="../assets/img/facebook.svg" alt=""
                        /></a>
                      </li>
                      <li class="social-list-item">
                        <a href="#"><img src="../assets/img/vk.svg" alt=""/> </a>
                      </li>
                      <li class="social-list-item">
                        <a href="#"
                        ><img src="../assets/img/telegram.svg" alt=""
                        /></a>
                      </li>
                      <li class="social-list-item">
                        <a href="#"><img src="../assets/img/youtube.svg" alt=""/></a>
                      </li>
                    </ul>
                    <div class="social-desc">
                      <p>
                        Проект ООО «Инитлаб», Краснодар, Россия.<br/>
                        Drupal является зарегистрированной торговой маркой Dries
                        Buytaert.
                      </p>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>

        </div>
      </div>
    </div>
  </div>
</template>

<script>
import AppForm from "@/components/AppForm.vue";

export default {
  name: "AppFooter",
  components: {AppForm},

}
</script>

<style>


.footer-region {
  position: relative;
  width: 100%;
  height: auto;
  background: linear-gradient(
      261.2deg,
      rgba(255, 255, 255, 0.276) -114.85%,
      rgba(255, 255, 255, 0) 69.04%
  ),
  url("../assets/img/druplar-emblem.svg") top center, url("../assets/img/druplar-emblem2.png") bottom right,
  #040613;
  background-repeat: no-repeat;
  background-size: cover, 220px, 220px;
  padding-top: 35px;
  padding-bottom: 45px;
}


.footer-region-background {
  position: absolute;
  z-index: -2;
  background: linear-gradient(254.72deg, rgba(255, 255, 255, .276) -114.85%, rgba(255, 255, 255, 0) 69.04%), #040613;
  left: 0;
  right: 0;
  top: 0;
  bottom: 0;
}

.phone {
  font-size: 24px;
  position: relative;
  text-decoration: none;
  color: #fff;
}

.email {
  position: relative;
  font-weight: bold;
  font-size: 20px;
  line-height: 150%;
  text-decoration-line: underline;

}

.form-control {
  color: #fff;
  background-color: transparent;
  border: 1px solid rgba(255, 255, 255, 0.3);
  box-sizing: border-box;
  border-radius: 5px;
  padding: 13px 12px;
  margin-bottom: 7px;

}

.form-control::placeholder {
  font-weight: 500;
  font-size: 14px;
  line-height: 16px;
  color: #fff;
  opacity: 1;
}

.form-control:focus {
  color: #f7f7f7;
  background-color: transparent;
  border-color: #ff2200;
  outline: 0;
  box-shadow: 0 0 0 0.25rem transparent;
}

.info textarea {
  background-color: #040613;
}

.form-group {
  width: 100%;
  margin-left: 60px;
}

.text-head-footer {
  font-weight: bold;
  font-size: 42px;
  color: #fff;

}

.form-politics {
  color: #ad1700;
  text-decoration: none;
  margin-left: 0px;
}

.form-politics:hover {
  color: #e76652;
  text-decoration: underline;
}

.text-extra-footer {
  line-height: 1.55;
  font-weight: 500;
  font-size: 14px;
  color: rgba(256, 256, 256, .7);
  margin-bottom: 140px;
}

.btn-footer {
  border: 2px solid #f14d34;
  border-radius: 5px;
  color: #fff;
  text-transform: uppercase;
  width: 100%;
  height: 50px;
  font-weight: 500;
  font-size: 12px;
  transition: background 300ms;
  background: #f14d34;
}

.btn-footer:hover {
  background-color: #fa735f;
}

.footer-social {
  position: relative;
  padding-top: 60px;

}

.footer-social:before {
  margin-top: 20px;
  content: "";
  position: absolute;
  display: block;
  left: 0;
  top: 0;
  right: 0;
  height: 1px;
  background-color: rgba(255, 255, 255, 0.3);
}

.social-list {
  list-style: none;
  display: flex;
  padding-left: 0px;
}

.social-list-item {
  display: inline-block;
  margin-right: 10px;
}

.social-list-item a {
  width: 30px;
  height: 30px;
  background: #f14d34;
  display: inline-block;
  text-align: center;
  border-radius: 5px;
}

.social-list-item img {
  width: 18px;
  height: 16px;
  filter: invert(1);
}
.form-row{
  color:#fff;
}

.social-desc {
  font-weight: normal;
  font-size: 14px;
  line-height: 17px;
  color: #ffffff;
  opacity: 0.5;
}

@media (max-width: 440px) {
  .footer-social {
    position: relative;
  }
  Form{
    margin-top: 30px;
  }

  .form-group {
    width: 100%;
    margin-left: 0px;
  }

  .btn-footer {
    margin-left: 0px;
  }

  .social-desc p {
    text-shadow: 1px 0 1px #000,
    0 1px 1px #000,
    -1px 0 1px #000,
    0 -1px 1px #000;
    color: #fff;
    opacity: 1000%;
    font-size: 14px;
    font-stretch: ultra-expanded;

  }

  .text-head-footer {
    font-size: 28px;
    margin-top: 80px;
  }

  .text-extra-footer {
    margin-top: 30px;
    font-size: 14px;
    margin-bottom: 40px;
  }

}


</style>
