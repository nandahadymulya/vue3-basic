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
    discount: {
      get() {
        return parseInt(this.number1) + parseInt(this.number2);
      },
      set(value) {
        this.number1 -= value;
        this.number2 -= value;
      },
    },
  },
  methods: {
    addDiscount() {
      this.discount = 500;
    },
  },
};
</script>

<template>
  <div>
    <input v-model="number1" type="text" /> <br />
    <input v-model="number2" type="text" />
    <button @click="addDiscount">discount</button>
  </div>
  <div>
    <h1>{{ discount }}</h1>
  </div>
</template>

<style scoped></style>
