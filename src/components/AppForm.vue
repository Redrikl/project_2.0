<template>
  <transition name="fade" @before-enter="beforeEnter" @enter="enter" @leave="leave">
    <form v-if="showForm" @submit.prevent="submitForm" id="Form">
      <div class="form-row">
        <div class="col-12">
          <input v-model="formData.lastName" class="form-control opacity-75 p-4 form-control-md info" type="text" name="lastName" placeholder="Ваше имя" autocomplete required>
        </div>
        <div class="col-12">
          <input v-model="formData.userPhone" class="form-control opacity-75 p-4 form-control-md info" type="text" name="userPhone" placeholder="Телефон" autocomplete pattern="[0-9+]+" required>
        </div>
        <div class="col-12">
          <input v-model="formData.userEmail" class="form-control opacity-75 p-4 form-control-md info" type="email" name="userEmail" placeholder="E-mail" required autocomplete>
        </div>
        <div class="col-12">
          <textarea v-model="formData.userMsg" class="form-control opacity-75 p-4 form-control-md info" name="userMsg" placeholder="Ваш комментарий"></textarea>
        </div>
        <div class="col-12">
          <input v-model="formData.agree" type="checkbox" id="check" required class="info">
          Согласен с
          <a class="form-politics" href="#" rel="nofollow">
            политикой обработки персональных данных
          </a>
        </div>
        <div class="col-12 mt-3">
          <button :disabled="isLoading" class="btn btn-footer" type="submit" @click="openForm" id="Button">
            <span v-if="isLoading" class="spinner-border spinner-border-sm" role="status" aria-hidden="true"></span>
            <span v-else>Свяжитесь с нами!</span>
          </button>
        </div>
      </div>
    </form>
  </transition>
  <transition name="fade" @before-enter="beforeEnter" @enter="enter" @leave="leave">
    <div v-if="isFormSubmitted" class="col-12 mt-3 text-success">
      Форма успешно отправлена!
    </div>
    <div v-else-if="errorMessage" class="error-message">{{ errorMessage }}</div>
  </transition>
</template>

<script>
import axios from 'axios';

export default {
  data() {
    return {
      showForm: true,
      isLoading: false,
      isFormSubmitted: false,
      errorMessage: '',
      formData: {
        lastName: '',
        userPhone: '',
        userEmail: '',
        userMsg: '',
        agree: false,
      },
    };
  },
  methods: {
    saveFormDataToLocalStorage() {
      localStorage.setItem('formData', JSON.stringify(this.formData));
    },

    loadFormDataFromLocalStorage() {
      const savedFormData = localStorage.getItem('formData');
      if (savedFormData) {
        this.formData = JSON.parse(savedFormData);
      }
    },

    async submitForm() {
      try {
        this.isLoading = true;

        const formData = new FormData();
        Object.keys(this.formData).forEach(key => {
          formData.append(key, this.formData[key]);
        });

        await axios.post('https://formcarry.com/s/b6wYF2ZycZN', formData);

        this.isFormSubmitted = true;
        this.isLoading = false;

        localStorage.removeItem('formData');
      } catch (error) {
        console.error('Ошибка:', error);
        this.isLoading = false;
        this.errorMessage =
          'Ошибка при отправке формы. Пожалуйста, попробуйте еще раз.';

        this.saveFormDataToLocalStorage();
      }
    },

    beforeEnter(el) {
      el.style.opacity = 0;
    },
    enter(el, done) {
      let opacity = 0;
      const duration = 500;

      function animate() {
        opacity += 1 / (duration / 16);
        el.style.opacity = opacity;

        if (opacity < 1) {
          requestAnimationFrame(animate);
        } else {
          done();
        }
      }

      animate();
    },
    leave(el, done) {
      let opacity = 1;
      const duration = 500;

      function animate() {
        opacity -= 1 / (duration / 16);
        el.style.opacity = opacity;

        if (opacity > 0) {
          requestAnimationFrame(animate);
        } else {
          done();
        }
      }
      animate();
    },
  },
};
</script>

<style scoped>
.error-message {
  color: red;
  margin-top: 10px;
}
.btn-footer {
  background: #f14d34;
  color: #fff;
}
.btn-footer:hover {
  background: #d13018;
}
</style>