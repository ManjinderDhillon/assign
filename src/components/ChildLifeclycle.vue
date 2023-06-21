<template>
  <h3>Hello Child Component</h3>
</template>
<script setup>
import {
  onBeforeMount,
  onMounted,
  onBeforeUpdate,
  onUpdated,
  onBeforeUnmount,
  onUnmounted,
} from "vue";

onBeforeMount(() => {
  console.log("onBeforeMount Called - child");
});
onMounted(() => {
  console.log("onMounted Called - child");
});
onBeforeUpdate(() => {
  console.log("onBeforeUpdate Called - child");
});
onUpdated(() => {
  console.log("onUpdated Called - child");
});
onBeforeUnmount(() => {
  console.log("onBeforeMount Called - child");
});
onUnmounted(() => {
  console.log("onBeforeMount Called - child");
});
</script>
