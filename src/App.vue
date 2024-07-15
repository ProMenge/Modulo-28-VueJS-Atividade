<script setup>
import { reactive, computed } from 'vue';
import CoalculatorHeader from './components/CalculatorHeader.vue';

const state = reactive({
  operator: "+",
  value1: '',
  value2: '',
});
</script>

<template>
  <div class="container">
    <CoalculatorHeader />
  </div>
</template>

<style lang="scss" scoped></style>
