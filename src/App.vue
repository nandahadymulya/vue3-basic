<script>
import ChildComponent from "./components/ChildComponent.vue";

export default {
  components: {
    ChildComponent,
  },
};
</script>

<template>
  <ChildComponent>
    <!-- <template v-slot:default="props"> -->
    <template v-slot:default="{ data }">
      <h1>Header</h1>
      <!-- <span>Title: {{ props.data }} </span> -->
      <span>Title: {{ data }} </span>
    </template>
    <template v-slot:main>
      <h1>Main</h1>
    </template>
    <template v-slot:section>
      <h1>Section</h1>
    </template>
    <template v-slot:footer>
      <h1>Footer</h1>
    </template>
  </ChildComponent>
</template>
