<script>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
import ChildComponent from "./components/ChildComponent.vue";

export default {
  components: { ChildComponent },
  data() {
    return {
      todos: ["one", "two", "three"],
      message: "Hello from props data!",
    };
  },
};
</script>

<template>
  <h1>Parent App</h1>
  <ChildComponent v-for="todo in todos" :key="todo" :message="todo" />
</template>

<style scoped></style>
