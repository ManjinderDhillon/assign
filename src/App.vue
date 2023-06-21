<template>
  <Directives />
  <ComputedComponent />
  <WatchComponent />
  <LifeCycle />
</template>
<script>
export default {
  name: "App",
};
</script>
<script setup>
import Directives from "./components/DirectivesComponent.vue";
import ComputedComponent from "./components/ComputedComponent.vue";
import WatchComponent from "./components/WatchComponent.vue";
import LifeCycle from "./components/LifeCycle.vue";
</script>
