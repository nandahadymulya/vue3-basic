<script>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
import ChildComponent from "./components/ChildComponent.vue";

export default {
  components: { ChildComponent },
};
</script>

<template>
  <h1>Parent App</h1>
  <ChildComponent />
  <child-component />
</template>

<style scoped></style>
