<template>
  <div class="result-container text-center mt-4">
    <p class="result-label h4">Result:</p>
    <p class="result-value display-4">{{ result }}</p>
  </div>
</template>

<script setup>
const props = defineProps(['result']);
</script>

<style scoped>
.result-label {
  color: #333;
}

.result-value {
  color: #007bff;
}
</style>
