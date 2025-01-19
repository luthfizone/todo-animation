<script setup>
const props = defineProps({
  message: String,
  style: Object,
});
</script>
<template>
  <button class="btn" :style="props.style">
    {{ props.message }}
  </button>
</template>

<style scoped>
.btn {
  border-radius: 5px;
  border: 1px solid #ccc;
  cursor: pointer;
  text-transform: uppercase;
  font-weight: bolder;
  align-self: center;
  padding: 5px 10px;
}

@media screen and (max-width: 600px) {
  .btn {
    padding: 5px 10px;
  }
}

@media screen and (min-width: 768px) {
  .btn {
    padding: 10px 15px;
  }
}
</style>
