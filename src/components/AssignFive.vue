<template>
  <h1>Tasks</h1>
  <input type="text" v-model="enteredTask" />
  <button @click="addTask">Add Task</button>
  <ul v-if="val === true">
    <li v-for="task in tasks" :key="task">{{ task }}</li>
  </ul>
  <button @click="toggleTask">Show/Hide</button>
</template>
<script setup>
import { ref } from "vue";

const enteredTask = ref("");
const tasks = ref([]);
const val = ref(true);
const addTask = () => {
  tasks.value.push(enteredTask.value);
};
const toggleTask = () => {
  val.value = !val.value;
};
</script>
