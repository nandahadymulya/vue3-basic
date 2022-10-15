<script>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
export default {
  data() {
    return {
      message: "is true.",
      status: false,
    };
  },
  methods: {
    toggleStatus() {
      this.status = !this.status;
    },
  },
};
</script>

<template>
  <button @click="toggleStatus">Change Status</button>
  <h1 v-if="status">{{ message }}</h1>
  <h1 v-else>is false.</h1>
</template>

<style scoped></style>
