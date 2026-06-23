<script setup lang="ts">
import type { Task } from '@/types/task.types';

defineProps<{ task: Task }>();
</script>

<template>
  <li class="task-item">
    <p>{{ task.name }}</p>
    <p class="description">{{ task.description }}</p>
  </li>
</template>

<style scoped>
.task-item {
  display: flex;
  align-items: center;
  flex-direction: column;
  gap: 10px;
  border: 1px solid black;
  border-radius: 10px;
  padding: 10px;
  width: 150px;
  overflow-wrap: break-word;
  word-break: break-word;
}

.description {
  font-size: 14px;
}
</style>
