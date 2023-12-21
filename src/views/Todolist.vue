<template>
  <div class="container bg-gradient-to-r from-cyan-600 to-cyan-800 ">
    <div class="title ">
      <h1>🚀 Todo App</h1>
    </div>
    <div class="actions">
      <form @submit.prevent="addTask">
        <input
          type="text"
          placeholder="Add Task"
          v-model="task"
          required
          class="task-input"
        />
        <button type="submit" class="add-btn">Add</button>
        <input
          type="text"
          placeholder="Search Task"
          v-model="searchQuery"
          class="search-input"
        />
      </form>
    </div>
    <div class="tasks">
      <div
        class="task-items"
        v-for="todo in filteredTasks"
        :key="todo.id"
        @click="doneTask(todo.id)"
      >
        <p :class="{ done: todo.status }">{{ todo.details }}</p>
        <button class="done-btn">Done</button>
        <button class="remove-btn" @click="removeTask(todo.id)">Remove</button>
      </div>
      <button class="clear-btn" @click="clearTasks">Clear All Tasks</button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      task: "",
      searchQuery: "",
      tasks: [],
    };
  },
  computed: {
    filteredTasks() {
      return this.tasks.filter((todo) =>
        todo.details.toLowerCase().includes(this.searchQuery.toLowerCase())
      );
    },
  },
  methods: {
    addTask() {
      if (this.task.trim() !== "") {
        this.tasks.push({
          id: Date.now(),
          details: this.task,
          status: false,
        });
        this.task = "";
      }
    },
    doneTask(id) {
      const index = this.tasks.findIndex((todo) => todo.id === id);
      if (index !== -1) {
        this.$set(this.tasks, index, {
          ...this.tasks[index],
          status: !this.tasks[index].status,
        });
      }
    },
    removeTask(id) {
      this.tasks = this.tasks.filter((todo) => todo.id !== id);
    },
    clearTasks() {
      this.tasks = [];
    },
  },
};
</script>

<style scoped>
.container {
  max-width: 400px;
  margin: auto;
  padding: 20px;
  background-color: #3498db;
  border-radius: 10px;
  box-shadow: 0 0 20px rgba(0, 0, 0, 0.2);
  color: #fff;
  align-items: absolute;
}

.title {
  text-align: center;
  margin-bottom: 20px;
  font-size: 28px;
  color: #ecf0f1;
}

.task-input,
.search-input {
  padding: 12px;
  border: 1px solid #2980b9;
  border-radius: 8px;
  margin-right: 10px;
  flex: 1;
  color: #2c3e50;
  background-color: #ecf0f1;
  margin-bottom:10px;
  
}

.add-btn,
.done-btn,
.remove-btn,
.clear-btn {
  padding: 12px;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  margin-top: 10px;
  transition: background-color 0.3s ease;
}

.add-btn {
  background-color: #27ae60;
  color: white;
}

.done-btn {
  background-color: #3498db;
  color: white;
}

.remove-btn {
  background-color: #e74c3c;
  color: white;
}

.clear-btn {
  background-color: #f39c12;
  color: white;
}

.done {
  text-decoration: line-through;
  color: #aaa;
}
</style>
