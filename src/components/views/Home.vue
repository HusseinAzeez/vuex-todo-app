<template>
  <div>
    <FilterTodos/>
    <AddTodo/>
    <TodoList/>
  </div>
</template>

<script>
import AddTodo from "../AddTodo";
import TodoList from "../TodoList";
import FilterTodos from "../FilterTodos";

export default {
  name: "Home",
  components: {
    AddTodo,
    TodoList,
    FilterTodos
  }
};
</script>

<style scoped>
</style>
