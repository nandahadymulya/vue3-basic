<script>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup

export default {
  data() {
    return {
      number1: 0,
      number2: 0,
    };
  },
  computed: {
    sum() {
      return parseInt(this.number1) + parseInt(this.number2);
    },
  },
};
</script>

<template>
  <div>
    <input v-model="number1" type="text" />
    <input v-model="number2" type="text" />
  </div>
  <h1>By Data</h1>
  <p>{{ parseInt(number1) + parseInt(number2) }}</p>

  <h1>By Computed</h1>
  {{ sum }}
</template>

<style scoped></style>
