<script>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
export default {
  data() {
    return {
      message: "Hello Nanda!",
    };
  },
};
</script>

<template>
  <h1>{{ message }}</h1>
  <input v-model="message" />
  <!-- same with belows -->
  <input :value="message" @input="message = $event.target.value" />
</template>

<style scoped></style>
