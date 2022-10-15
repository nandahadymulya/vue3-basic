<script>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
export default {
  data() {
    return {
      count: 0,
      message: "Hello Nanda!",
    };
  },
  methods: {
    increment() {
      this.count += 2;
    },
  },
};
</script>

<template>
  <div>Message is: {{ message }}</div>
  <br />
  <h1 :title="message">What's the message ? (Hover)</h1>
  <br />
  <h1>{{ count }}</h1>
  <button @click="count++">+ 1</button>
  <button @click="increment">Increment 2 by methods</button>
</template>

<style scoped></style>
