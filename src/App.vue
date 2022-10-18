<script>
import basicMixins from "./mixins/basic";
import mergeMixins from "./mixins/merge";

export default {
  mixins: [basicMixins, mergeMixins],
  data() {
    return {
      name: "Nanda",
    };
  },
};
</script>

<template>
  <pre>{{ $data }}</pre>
  <button @click="onClick">Click</button>
</template>
