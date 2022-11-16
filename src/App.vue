<script>
import TodoList from "./components/TodoList.vue";

export default {
  components: { TodoList },
  data() {
    return {
      todo: "",
      todos: [],
    };
  },
  computed: {
    countTodo() {
      return this.todos.length;
    },
  },
  mounted() {
    this.todos = JSON.parse(localStorage.getItem("todos")) || [];
  },
  methods: {
    createTodo() {
      // this.todos.push(this.todo);
      this.todos.unshift({
        activity: this.todo,
        status: false,
      });
      this.todo = "";
      this.saveToLocal();
    },
    deleteTodo(todoIndex) {
      this.todos = this.todos.filter((todo, index) => {
        if (index != todoIndex) {
          return todo;
        }
      });
      this.saveToLocal();
    },
    doneTodo(todoIndex) {
      this.todos = this.todos.map((todo, index) => {
        if (index == todoIndex) {
          todo.status = !todo.status;
        }
        return todo;
      });
      this.saveToLocal();
    },
    saveToLocal() {
      localStorage.setItem("todos", JSON.stringify(this.todos));
    },
  },
};
</script>

<template>
  <div class="container-fluid bg-light rounded-lg vh-100">
    <div class="row p-5 text-center">
      <div class="col">
        <h1 class="fw-bold">Simple Todo App</h1>
        <p class="text-muted">Developed using Vue 3 Options API.</p>
      </div>
    </div>

    <div class="row justify-content-center">
      <div class="col-md-10 mb-3">
        <div class="d-flex gap-1 m-1">
          <input class="form-control" v-model="todo" @keyup.enter="createTodo" type="text" placeholder="Add new todo" />
          <button class="btn btn-primary" @click="createTodo">Add</button>
        </div>
      </div>

      <div class="col-md-10 mb-3">
        <div class="badge bg-info float-end m-1">Total: {{ countTodo }}</div>
      </div>

      <TodoList :todos="todos" @parsingIndexDelete="deleteTodo" @parsingIndexDone="doneTodo" />
    </div>
  </div>
</template>
