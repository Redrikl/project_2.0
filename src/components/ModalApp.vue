<template>
  <b-modal id="exampleModal" title="Modal Title" :visible="modalVisible" @hide="hideModal">
    <AppForm />
  </b-modal>
</template>

<script>
import AppForm from "@/components/AppForm.vue";

export default {
  components: { AppForm },
  data() {
    return {
      modalVisible: false,
    };
  },
  methods: {
    showModal() {
      this.modalVisible = true;
    },
    hideModal() {
      this.modalVisible = false;
    },
  },
};
</script>

<style>
.modal__content {
  padding: 40px;
  background: #040613 !important;
}
.modal__width {
  width: 700px !important;
}
@media (max-width: 440px) {
  .modal__width {
    width: 375px !important;
  }
}
</style>