<template>
  <header>
    <h1>TODO LIST</h1>
    <button @click="showModal = true">ADD</button>
  </header>

  <div class="todo-card-wrapper">
    <TodoCard
      v-for="task in todo"
      :key="task.id"
      :task="task"
      @removeTask="removeTask"
    />
  </div>

  <TaskModal
    v-if="showModal"
    @closeModel="clearModalData"
    @submitForm="addTaskInTodo"
  />
</template>

<style scoped>
* {
  font-family: Arial, sans-serif;
  margin: 0px;
  padding: 0px;
  box-sizing: border-box;
}
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px;
  background-color: rebeccapurple;
  border-bottom: 1px solid #ccc;
  margin-bottom: 20px;
}
header button {
  padding: 5px 10px;
  border: none;
  background-color: red;
  color: white;
  cursor: pointer;
}
.todo-card-wrapper {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-gap: 20px;
  margin-top: 20px;
}
</style>

<script>
import TaskModal from "./components/TaskModal.vue";
import TodoCard from "./components/TodoCard.vue";
export default {
  components: {
    TaskModal,
    TodoCard,
  },
  data() {
    return {
      showModal: false,
      todo: [
        { id: 1, title: "Task 1", description: "Lorem ipsum dolor sit amet" },
        { id: 2, title: "Task 2", description: "Lorem ipsum dolor sit amet" },
        { id: 3, title: "Task 3", description: "Lorem ipsum dolor sit amet" },
        { id: 4, title: "Task 4", description: "Lorem ipsum dolor sit amet" },
      ],
    };
  },
  methods: {
    addTaskInTodo(task) {
      const randomId = Math.floor(Math.random() * this.todo.length);
      console.log(randomId);
      console.log(task);
      if (task.title && task.description) {
        const newTask = {
          id: randomId,
          title: task.title,
          description: task.description,
        };
        this.todo.push(newTask);
        this.showModal = false;
      } else {
        alert("Please fill out both title and description.");
      }
    },
    clearModalData() {
      this.newData = { title: "", description: "" };
      this.showModal = false;
    },
    removeTask(taskId) {
      this.todo = this.todo.filter((task) => task.id !== taskId);
    },
  },
};
</script>
