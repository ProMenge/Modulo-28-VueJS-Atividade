<template>
  <div class="row align-items-center justify-content-center">
    <div class="col">
      <label for="input1">Número 1:</label>
      <br>
      <input type="number" id="input1" @input="setValue1" />
    </div>

    <div class="col">
      <label for="input2">Número 2:</label>
      <br>
      <input type="number" id="input2" @input="setValue2" />
    </div>
  </div>

  <div class="row justify-content-center mt-5">
    <h4>Operation</h4>
  </div>

  <div class="row justify-content-center mt">
    <select @change="changeOperatorAndDoTheMath" name="" id="" class="form-control w-50 text-center">
      <option value="plus">+</option>
      <option value="minus">-</option>
      <option value="multiply">*</option>
      <option value="division">/</option>
    </select>
  </div>
</template>

<script setup>
const props = defineProps(['setValue1', 'setValue2', 'changeOperatorAndDoTheMath'])
</script>

<style scoped></style>
