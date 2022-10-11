<script setup lang="ts">
import { computed, ref } from "vue";

defineProps<{
  name: string;
}>();

const count = ref(0);
function increment() {
  count.value++;
}

const double = computed(() => count.value * 2);
</script>

<template>
  <div>
    <h1 class="title">Hello {{ name }} from Inertia + Django + Vite + Vue!</h1>
    <button @click="increment">Add</button>
    <p>Count: {{ count }}</p>
  </div>
</template>

<style scoped>
.title {
  color: green;
}
</style>
