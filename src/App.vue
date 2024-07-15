<script setup>
import { reactive } from 'vue';
import CalculatorHeader from './components/CalculatorHeader.vue';
import Form from './components/Form.vue';
import Result from './components/Result.vue';

const state = reactive({
  operator: "plus",
  value1: '',
  value2: '',
  result: ''
});

const setValue1 = (event) => {
  state.value1 = Number(event.target.value);
  console.log('Value 1:', state.value1);
  calculateResult();
}

const setValue2 = (event) => {
  state.value2 = Number(event.target.value);
  console.log('Value 2:', state.value2);
  calculateResult();
}

const changeOperatorAndDoTheMath = (event) => {
  state.operator = event.target.value;
  console.log('Operator:', state.operator);
  calculateResult();
}

const calculateResult = () => {
  switch (state.operator) {
    case 'plus':
      state.result = state.value1 + state.value2;
      break;
    case 'minus':
      state.result = state.value1 - state.value2;
      break;
    case 'multiply':
      state.result = state.value1 * state.value2;
      break;
    case 'division':
      state.result = state.value2 !== 0 ? state.value1 / state.value2 : 'Error';
      break;
  }
  console.log('Result:', state.result);
}
</script>

<template>
  <div class="container display-flex text-center pb-4  ">
    <CalculatorHeader />
    <Form :set-value1="setValue1" :set-value2="setValue2"
      :change-operator-and-do-the-math="changeOperatorAndDoTheMath" />
    <Result :result="state.result" />

  </div>
</template>

<style lang="scss" scoped>
.container {
  border: 2px black solid;
}
</style>
