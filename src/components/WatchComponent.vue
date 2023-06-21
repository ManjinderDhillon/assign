<template>
  <div>{{ count }}</div>
  <button @click="add">Add</button>
  <button @click="sub">Sub</button>
</template>

<script setup>
import { ref, watch } from "vue";
const count = ref(0);

watch(count, (newval) => {
  if (newval > 5) {
    return alert("Stop Adding");
  }
});
const add = () => {
  count.value = count.value + 1;
};
const sub = () => {
  count.value = count.value - 1;
};
</script>
