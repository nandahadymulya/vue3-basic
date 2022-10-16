<script>
import ChildComponent from "./components/ChildComponent.vue";

export default {
  components: {
    ChildComponent,
  },
  data() {
    return {
      message: "On Parent!",
      value: "Message from Parent!",
    };
  },
  methods: {
    changeMessage(value) {
      this.message = value;
    },
    clickThis(value) {
      this.$refs.childComponent.changeMessage(value);
    },
  },
};
</script>

<template>
  <ChildComponent ref="childComponent" @child-event="changeMessage" :message="message" />

  <button @click="clickThis(value)">Click from parent</button>
</template>
