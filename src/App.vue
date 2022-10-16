<script>
import ComponentOne from "./components/ComponentOne.vue";
export default {
  components: {
    ComponentOne,
  },
  data() {
    return {
      author: "Nanda Hady Mulya",
    };
  },
  provide() {
    return {
      providedAuthor: this.author,
    };
  },
};
</script>

<template>
  <h1>Parent</h1>
  <component-one />
</template>
