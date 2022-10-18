<script>
import HomeComponent from "./components/Home.vue";

export default {
  components: {
    HomeComponent,
  },
};
</script>

<template>
  <teleport to="#teleport">
    <HomeComponent />
  </teleport>
</template>
