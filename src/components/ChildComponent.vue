<script>
export default {
  props: {
    title: String,
    number: {
      type: Number,
      default: 0,
    },
  },
};
</script>

<template>
  <h1>{{ title }}</h1>
  <h2>{{ number }}</h2>
</template>
