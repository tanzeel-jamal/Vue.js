<template>
  <div class="todo-card">
    <div class="title">
      <h3>{{ task.title }}</h3>
      <button @click="$emit('removeTask', task.id)">Remove</button>
    </div>
    <p>{{ task.description }}</p>
  </div>
</template>

<script>
export default {
  props: {
    task: Object,
  },
  emits: ["removeTask"],
};
</script>

<style scoped>
.todo-card {
  padding: 15px;
  border: 1px solid #ccc;
  border-radius: 5px;
  margin-bottom: 10px;
  background-color: aqua;
}
.todo-card .title {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 40px;
}
.todo-card .title button {
  padding: 5px 10px;
  border: none;
  background-color: blue;
  color: white;
  cursor: pointer;
}
</style>
