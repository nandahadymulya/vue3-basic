<script>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
export default {
  data() {
    return {
      todos: [
        {
          id: 1,
          title: "Todo One",
        },
        {
          id: 2,
          title: "Todo Two",
        },
      ],
    };
  },
};
</script>

<template>
  <ol v-for="(todo, index) in todos" :key="todo.id">
    <li>{{ index }} - {{ todo.title }}</li>
  </ol>
</template>

<style scoped></style>
