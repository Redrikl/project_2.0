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