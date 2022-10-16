<script>
export default {
  props: ["modelValue"],
};
</script>
<template>
  <h2>Child Component:</h2>
  <input :value="modelValue" @input="$emit('update:modelValue', $event.target.value)" />
</template>
