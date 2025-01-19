<script setup>
import Header from "@/components/Header.vue";
import InputUser from "@/components/InputUser.vue";
import TodoContent from "@/components/TodoContent.vue";
import tasks from "@/data/data.js";
</script>

<template>
  <main>
    <Header />
    <InputUser />
    <TodoContent :tasks="tasks" />
  </main>
</template>
