<template>
  <div>
    {{ data }}
  </div>
</template>
<script setup>
import { computed, ref } from "vue";
const doller = ref(80);
const Rupees = ref(200);
const tax = ref(30);
const data = computed(() => {
  return doller.value + Rupees.value * tax.value;
});
</script>
