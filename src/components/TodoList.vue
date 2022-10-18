<script>
export default {
  props: {
    todo: String,
    todos: {
      type: Array,
      default: [],
    },
  },
  methods: {
    parsingIndexDelete(index) {
      this.$emit("parsingIndexDelete", index);
    },
    parsingIndexDone(index) {
      this.$emit("parsingIndexDone", index);
    },
  },
};
</script>
<template>
  <div class="col-md-10 mb-3">
    <ul class="list-group" v-for="(todo, index) in todos" :key="index">
      <li class="list-group-item m-1">
        <div class="d-flex justify-content-between align-items-center">
          <div>
            <span v-if="todo.status">
              <del class="text-muted">{{ todo.activity }}</del>
            </span>
            <span v-else>
              <span>{{ todo.activity }}</span>
            </span>
          </div>
          <div>
            <button class="btn btn-danger btn-sm me-1" @click="parsingIndexDelete(index)">Delete</button>
            <button class="btn btn-success btn-sm" @click="parsingIndexDone(index)">Done</button>
          </div>
        </div>
      </li>
    </ul>
  </div>
</template>
