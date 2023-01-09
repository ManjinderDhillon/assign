<template>
  <p>{{ userInput }}</p>
  <input type="text" v-on:keyup="setInput" id="" />
  <p>{{ confirm }}</p>
  <input type="text" v-on:keydown.enter="confirmInput" />
</template>
<script>
export default {
  name: "HelloWorld",
};
</script>
<script setup>
import { ref } from "vue";

const userInput = ref("");
const confirm = ref("");
const setInput = (event) => {
  userInput.value = event.target.value;
};
const confirmInput = (event) => {
  confirm.value = event.target.value;
};
</script>
