<script setup>
import { ref } from "vue";

const showText = ref(false);
</script>

<template>
  <main>
    <Transition name="fade">
      <h1 v-if="showText">Hello World</h1>
    </Transition>
    <button @click="showText = !showText">Toggle</button>
  </main>
</template>

<style scoped>
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s ease;
}
</style>
