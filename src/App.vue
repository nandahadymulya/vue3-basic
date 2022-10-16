<script>
import ChildComponent from "./components/ChildComponent.vue";

export default {
  components: {
    ChildComponent,
  },
  data() {
    return {
      message: "",
    };
  },
};
</script>

<template>
  <h1>Event: {{ message }}</h1>
  <hr />
  <ChildComponent :model-value="message" @update:model-value="message = $event" />

  <hr />
  <ChildComponent v-model="message" />
</template>
