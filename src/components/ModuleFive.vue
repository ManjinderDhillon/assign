<template>
  <input type="text" name="" id="" @input="saveInput" />
  <button @click="setText">setText</button>
  <h1>{{ message }}</h1>
</template>
<script setup>
import { ref } from "vue";
const currentInput = ref("");
const message = ref("");
const saveInput = (event) => {
  currentInput.value = event.target.value;
};
const setText = () => {
  message.value = currentInput.value;
};
</script>
