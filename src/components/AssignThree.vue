<template>
  <button @click="addNum(5)">Add 5</button>
  <button @click="addNum(2)">Add 2</button>
  <p>{{ result }}</p>
</template>

<script setup>
import { ref } from "vue";
import { computed } from "@vue/reactivity";

const number = ref(0);
const result = computed(() => {
  if (number.value < 37) {
    return "Too Short";
  }
  if (number.value === 37) {
    return number.value;
  } else {
    return "Too Much";
  }
});

const addNum = (num) => {
  return (number.value = number.value + num);
};
</script>
