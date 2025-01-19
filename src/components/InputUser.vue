<script setup>
import { ref } from "vue";

import Button from "@/components/Button.vue";

// Add button
const messageAdd = "add";
const styleAddButton = {
  backgroundColor: "#41e457",
  color: "#fff",
};

// Emit / send data to parent component
const inputUser = ref("");
const emit = defineEmits(["addTask"]);

/**
 * This function will sending data with
 * parameter from InputUser ref
 * and this function will empty the ref again
 * after the function it called
 */
const addTask = () => {
  emit("addTask", inputUser.value);
  inputUser.value = "";
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
      v-model.lazy="inputUser"
    />
    <Button
      :message="messageAdd"
      :style="styleAddButton"
      :inputUser="inputUser"
      @click="addTask"
    />
  </div>
</template>

<style scoped>
.container {
  width: 50%;
  margin-bottom: 1.5rem;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: center;
  gap: 1rem;
}

.input-text {
  width: 88%;
  padding: 0.8rem;
  font-family: Arial, Helvetica, sans-serif;
  border-radius: 5px;
  border: 1px solid #ccc;
}

[type="text"] {
  padding-left: 1rem;
}

@media screen and (max-width: 600px) {
  .input-text {
    width: 60%;
  }
}

@media screen and (min-width: 768px) {
  .input-text {
    width: 70%;
  }
}
</style>
