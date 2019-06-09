<template>
  <div
    class="todo"
    v-bind:class="{'is-complete':todo.completed}"
    v-on:dblclick="handleDoubleClick(todo)"
  >
    {{todo.title}}
    <i v-on:click="deleteTodo(todo.id)" class="fas fa-trash-alt"></i>
  </div>
</template>

<script>
import { mapActions } from "vuex";
export default {
  name: "TodoItem",
  props: ["todo"],
  methods: {
    ...mapActions(["deleteTodo", "updateTodo"]),
    handleDoubleClick(todo) {
      const updatedTodo = {
        id: todo.id,
        title: todo.title,
        completed: !todo.completed
      };
      this.updateTodo(updatedTodo);
    }
  }
};
</script>

<style scoped>
.todo {
  position: relative;
  padding: 1rem;
  text-align: center;
  color: #fff;
  border: 1px solid #ccc;
  border-radius: 5px;
  background: #41b883;
  cursor: pointer;
}

i {
  position: absolute;
  bottom: 10px;
  right: 10px;
  color: #fff;
  cursor: pointer;
}

.is-complete {
  background: #35495e;
  color: #fff;
}
</style>
