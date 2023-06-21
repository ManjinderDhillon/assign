<template>
  <ChildLifeclycle v-if="togValue" />
  <button @click="toggle">Toggle</button>
  {{ count }}
  <button @click="add">Add</button>
</template>
<script setup>
import { ref } from "vue";
import ChildLifeclycle from "./ChildLifeclycle.vue";
import {
  onBeforeMount,
  onMounted,
  onBeforeUpdate,
  onUpdated,
  onBeforeUnmount,
  onUnmounted,
} from "vue";
const togValue = ref(true);
const count = ref(0);
onBeforeMount(() => {
  console.log("onBeforeMount Called - parent");
});
onMounted(() => {
  console.log("onMounted Called - parent");
});
onBeforeUpdate(() => {
  console.log("onBeforeUpdate Called - parent");
});
onUpdated(() => {
  console.log("onUpdated Called - parent");
});
onBeforeUnmount(() => {
  console.log("onBeforeMount Called - parent");
});
onUnmounted(() => {
  console.log("onBeforeMount Called - parent");
});
const toggle = () => {
  togValue.value = !togValue.value;
};
const add = () => {
  count.value += 1;
};
</script>
