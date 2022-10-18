<script>
export default {
  data() {
    return {
      posts: [],
    };
  },
  async created() {
    const res = await fetch("https://swapi.dev/api/planets/");
    const { results } = await res.json();
    this.posts = results;
  },
};
</script>
<template>
  <div class="tab-demo">
    Post Componets
    <div v-for="post in posts" :key="post">
      <p>{{ post.name }}</p>
    </div>
  </div>
</template>
