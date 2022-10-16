<script>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup

export default {
  data() {
    return {
      message: "Render Only One",
    };
  },
};
</script>

<template>
  <h1 v-once>{{ message }}</h1>
  <button @click="message = 'Rendering again.'">V-Once</button>
</template>

<style scoped></style>
