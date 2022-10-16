<script>
import ChildComponent from "./components/ChildComponent.vue";
export default {
  components: { ChildComponent },
};
</script>

<template>
  <child-component title="Nanda" :number="28" />
</template>
