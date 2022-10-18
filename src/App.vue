<script>
import Home from "./components/Home.vue";
import Post from "./components/Post.vue";
import About from "./components/About.vue";

export default {
  components: { Home, Post, About },
  data() {
    return {
      currentTab: "Home",
      tabs: ["Home", "Post", "About"],
    };
  },
  computed: {
    currentTabComponent() {
      return this.currentTab.toLowerCase();
    },
  },
};
</script>

<template>
  <div class="tab">
    <button v-for="tab in tabs" :key="tab" :class="['tab-button', { active: currentTab === tab }]" @click="currentTab = tab">
      {{ tab }}
    </button>
  </div>

  <keep-alive>
    <component :is="currentTabComponent" />
  </keep-alive>
</template>

<style>
.tab {
  border: 1px solid #eeeeee;
  border-radius: 2px;
  padding: 20px 30px;
  margin-top: 1em;
  margin-bottom: 40px;
  user-select: none;
  overflow-x: auto;
}
.tab-button {
  padding: 6px 10px;
  border-top-left-radius: 3px;
  border-top-right-radius: 3px;
  border: 1px solid #cccccc;
  cursor: pointer;
  background-color: #f0f0f0;
  margin-bottom: -1px;
  margin-right: -1px;
}
.tab-button:hover {
  background-color: #e0e0e0;
}
.tab-button:active {
  background-color: #d0d0d0;
}
.tab-demo {
  border: 1px solid #ccc;
  padding: 10px;
}
</style>
