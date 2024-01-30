<script setup lang="ts">
defineProps(["title"]);
</script>

<script lang="ts">
export default {
  methods: {
    closeModal() {
      this.$emit("close");
    },
  },
};
</script>

<template>
  <div class="backdrop" @click="closeModal">
    <div class="modal">
      <h2>{{ title }}</h2>
      <slot />
    </div>
  </div>
</template>

<style scoped>
h2 {
  margin-top: 0;
}

.modal {
  width: 400px;
  padding: 20px;
  margin: 100px auto;
  background: white;
  border-radius: 10px;
}

.backdrop {
  top: 0;
  left: 0;
  position: fixed;
  background: rgba(0, 0, 0, 0.35);
  width: 100%;
  height: 100%;
}
</style>
