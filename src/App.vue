<script>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup

export default {
  data() {
    return {
      message: "Test",
      status: true,
      boldClass: "bold",
      greenClass: "successed",
    };
  },
};
</script>

<template>
  <h1 :class="status ? 'successed' : 'failded'">{{ message }}</h1>
  <button @click="status = !status">Changed status</button>
  <h1 :class="[boldClass, greenClass]">{{ message }}</h1>
</template>

<style scoped>
.successed {
  color: green;
}
.failded {
  color: red;
}
.bold {
  font-weight: 100;
}
</style>
