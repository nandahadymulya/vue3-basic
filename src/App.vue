<script>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup

export default {
  data() {
    return {
      message: "Test",
    };
  },
  watch: {
    message(value) {
      console.log("Perubahan data message", value);
    },
  },
};
</script>

<template>
  <h1>{{ message }}</h1>
  <input v-model="message" />
</template>

<style scoped></style>
