<template>
  <dir>
    <div class="nav">
      <router-link to="/">Home</router-link>
      <router-link to="/about">About</router-link>
    </div>
    <h1>Todo List</h1>
  </dir>
</template>

<script>
export default {
  name: "Header"
};
</script>

<style scoped>
.nav {
  display: flex;
  flex-direction: row;
  justify-content: flex-end;
  font-size: 1.2rem;
}
a {
  margin: 0 1em;
  text-decoration: none;
  color: #000;
  cursor: pointer;
}
</style>
