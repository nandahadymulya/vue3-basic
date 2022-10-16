<script>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
import ChildComponent from "./components/ChildComponent.vue";

export default {
  data() {
    return {
      message: "First Message",
    };
  },

  beforeCreate() {
    console.log("beforeCreate");
  },
  created() {
    console.log("created");
    console.log(document.getElementById("lifecycle"));
    // console.log(document.getElementById("lifecycle").textContent);
    // fetch data from API
  },
  // after created component
  beforeMount() {
    console.log("beforeMount");
  },
  mounted() {
    console.log("mounted");
    console.log(document.getElementById("lifecycle"));
    console.log(document.getElementById("lifecycle").textContent);
    // process data
  },
  // re-render component
  beforeUpdate() {
    console.log("beforeUpdate");
    console.log(document.getElementById("lifecycle").textContent);
  },
  updated() {
    console.log("updated");
    console.log(document.getElementById("lifecycle").textContent);
  },
  // destroy component after move to component
  beforeUnmount() {
    console.log("beforeUnmount");
  },
  unmounted() {
    console.log("unmounted");
  },
};
</script>

<template>
  <h1>Parent App</h1>
  <p id="lifecycle">{{ message }}</p>
  <button @click="message = 'Re-rendering is running this.'">Updated</button>
</template>

<style scoped></style>
