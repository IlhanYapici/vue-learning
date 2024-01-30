<script setup lang="ts">
import Modal from "./components/Modal.vue";
</script>

<script lang="ts">
export default {
  data() {
    return {
      showModal: false,
    };
  },
  methods: {
    toggleModal() {
      this.showModal = !this.showModal;
    },
  },
};
</script>

<template>
  <h1>Hello there</h1>
  <Modal v-if="showModal" title="Modal" @close="toggleModal">
    good morning
  </Modal>
  <button @click="toggleModal">open modal</button>
</template>
