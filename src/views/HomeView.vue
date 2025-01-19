<script setup>
import { ref } from "vue";

import Header from "@/components/Header.vue";
import InputUser from "@/components/InputUser.vue";
import TodoContent from "@/components/TodoContent.vue";
import tasks from "@/data/data.js";

// Task list for initial value from tasks
const taskList = ref([...tasks]);

/**
 * This function for adding data
 * to taskList
 *
 * The data have been get from InputUser component
 * using emit @addTask
 */
const addTask = (newTask) => {
  taskList.value.push(newTask);
};
</script>

<template>
  <main>
    <Header />
    <InputUser @addTask="addTask" />
    <TodoContent :tasks="taskList" />
  </main>
</template>
