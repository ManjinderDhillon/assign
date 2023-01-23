<template>
  <h1>My Gosls</h1>
  <input type="text" v-model="goalName" />
  <button @click="addGoal">Add Goal</button>
  <p v-if="goals.length === 0">no goals added yet</p>
  <ul v-else>
    <li v-for="(goal, index) in goals" :key="goal" @click="removeGoal(index)">
      {{ goal }}-{{ index }}
    </li>
  </ul>
</template>
<script setup>
import { ref } from "vue";

const goalName = ref("");
const goals = ref([]);
const addGoal = () => {
  goals.value.push(goalName.value);
};
const removeGoal = (index) => {
  goals.value.splice(index, 1);
};
</script>
