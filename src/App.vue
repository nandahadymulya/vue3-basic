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
  <div>Message is: {{ message }}</div>
  <br />
  <h1 :title="message">What's the message ? (Hover)</h1>
  <br />
  <button @click="count++">+ 1</button>
</template>

<style scoped></style>
