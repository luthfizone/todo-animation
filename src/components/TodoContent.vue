<script setup>
const { tasks } = defineProps({
  tasks: Array,
});
</script>

<template>
  <div class="card-list">
    <div class="card" v-for="(task, index) in tasks" :key="index">
      {{ task }}
    </div>
  </div>
</template>

<style scoped>
.card-list {
  margin-top: 1.5rem;
  width: 40%;
  font-family: Arial, Helvetica, sans-serif;
}

.card {
  margin-top: 1rem;
  padding: 5% 10%;
  text-align: center;
  cursor: pointer;
  box-shadow: 1px 1px 10px rgba(0, 0, 0, 0.2);
}
</style>
