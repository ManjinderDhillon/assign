<template>
  <h1>This is The Parent Component</h1>
  <ChildComponent :name="name" @messageSent="handleMessage" />
  <p>Received message: {{ receivedMessage }}</p>
</template>
<script setup>
import { ref } from "vue";
import ChildComponent from "./ChildComponent.vue";
const name = ref("Child");
const receivedMessage = ref("");
const handleMessage = (message) => {
  receivedMessage.value = message;
};
</script>
