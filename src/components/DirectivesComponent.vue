<template>
  <h1>Tasks</h1>
  <input type="text" v-model="inputValue" />
  <button @click="addTask">Add</button>
  <ul v-if="val">
    <li v-for="task in tasks" :key="task">{{ task }}</li>
  </ul>
  <button @click="toggleTask">Show/Hide</button>
</template>
<script setup>
import { ref } from "vue";
const inputValue = ref("");
const tasks = ref([]);
const val = ref(true);
const addTask = () => {
  tasks.value.push(inputValue.value);
  inputValue.value = "";
};
const toggleTask = () => {
  val.value = !val.value;
};
</script>
