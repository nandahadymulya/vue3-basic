<script>
export default {
  props: ["modelValue"],
  computed: {
    value: {
      get() {
        return this.modelValue;
      },
      set(value) {
        this.$emit("update:modelValue", value);
      },
    },
  },
};
</script>
<template>
  <h2>Child Component:</h2>
  <!-- <input :value="modelValue" @input="$emit('update:modelValue', $event.target.value)" /> -->

  <input v-model="value" type="text" />
</template>
