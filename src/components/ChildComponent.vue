<script>
export default {
  // props: ["message"],
  data() {
    return {
      value: "Message from Child!",
    };
  },
  emits: ["child-event"],
  props: {
    message: {
      type: String,
      required: true,
    },
  },
  methods: {
    changeMessage(value) {
      this.$emit("child-event", value);
    },
  },
};
</script>
<template>
  <h2>Child Component:</h2>
  <p>{{ message }}</p>
  <button @click="changeMessage(value)">Click from child</button>
</template>
