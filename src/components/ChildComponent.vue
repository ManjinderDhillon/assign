<template>
  <h1>This is The Child Component</h1>
  {{ data }}
  <button @click="sendMessage">Send Message</button>
</template>
<script setup>
import { defineProps, ref, getCurrentInstance } from "vue";
const props = defineProps(["name"]);
const data = ref(props.name);

const instance = getCurrentInstance();

const sendMessage = () => {
  const message = "Hello, world!";
  instance.emit("messageSent", message);
};
</script>
