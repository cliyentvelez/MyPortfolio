<script setup>
import MainLayout from '../components/MainLayout.vue';

// Page Title of Views
const pageTitle = 'Projects'
</script>

<template>
  <MainLayout :pageTitle="pageTitle">
    <section>
      <!-- <div class="todo-app">
        <input v-model="newTodo" @keyup.enter="addTodo" placeholder="Add a new todo..." />
        <ul>
          <li v-for="(todo, index) in todos" :key="index">
            {{ todo }}
            <button @click="deleteTodo(index)">❌</button>
          </li>
        </ul>
      </div> -->
      <div class="mt-4 text-center">
        <router-link to="/todolist"
          class="inline-block rounded-lg bg-blue-500 text-white px-4 py-2 text-center text-sm font-semibold text-gray-500 outline-none ring-indigo-300 transition duration-100 hover:bg-pink-600 focus-visible:ring active:bg-pink-700 md:px-8 md:py-3 md:text-base">Todolist</router-link>
      </div>

      <!-- Button for your special app -->
      <div class="mt-4 text-center">
        <router-link to="/flowers"
          class="inline-block rounded-lg bg-green-500 text-white px-4 py-2 text-center text-sm font-semibold text-gray-500 outline-none ring-indigo-300 transition duration-100 hover:bg-pink-600 focus-visible:ring active:bg-pink-700 md:px-8 md:py-3 md:text-base">App Project</router-link>
      </div>

     
    </section>
  </MainLayout>
</template>

<script>
// import MainLayout from '@/components/MainLayout'; // Import your MainLayout component path

export default {
  components: {
    MainLayout,
  },
  data() {
    return {
      pageTitle: 'Todo App',
      newTodo: '',
      todos: [],
    };
  },
  methods: {
    addTodo() {
      if (this.newTodo.trim() !== '') {
        this.todos.push(this.newTodo);
        this.newTodo = '';
      }
    },
    deleteTodo(index) {
      this.todos.splice(index, 1);
    },
    handleSpecialApp() {
      // Implement functionality for your special app button
      // For example, you can add your specific logic here
      console.log('Special App button clicked!');
    },
  },
};
</script>

 
  