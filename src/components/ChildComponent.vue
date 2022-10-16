<script>
export default {
  // props: ["message"],
  props: {
    message: {
      type: String,
      required: true,
    },
  },
};
</script>
<template>
  <h2>Child Component:</h2>
  <p>{{ message }}</p>
</template>
