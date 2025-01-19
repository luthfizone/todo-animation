<script setup>
import Button from "@/components/Button.vue";

// Add button
const messageAdd = "add";
const styleAddButton = {
  backgroundColor: "#41e457",
  color: "#fff",
};
</script>

<template>
  <div class="container">
    <input
      type="text"
      name="todo"
      id="todo"
      class="input-text"
      placeholder="Add todo.."
    />
    <Button :message="messageAdd" :style="styleAddButton" />
  </div>
</template>

<style scoped>
.container {
  width: 75%;
  margin-bottom: 1.5rem;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  gap: 1rem;
}

.input-text {
  width: 90%;
  padding: 0.8rem;
  font-family: Arial, Helvetica, sans-serif;
  border-radius: 5px;
  border: 1px solid #ccc;
}

[type="text"] {
  padding-left: 1rem;
}
</style>
