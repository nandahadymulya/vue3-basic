<script>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup

export default {
  data() {
    return {
      message: `<span style="color: red">Rendering v-html</span>`,
    };
  },
};
</script>

<template>
  <div>
    {{ message }}
  </div>
  <div v-html="message"></div>
</template>

<style scoped></style>
