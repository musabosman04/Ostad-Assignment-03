<script setup>
import Calculator from './components/Calculator.vue';
import Quotation from './components/Quotation.vue';
</script>

<template>
  <div class="flex">

    <div class="h-screen flex items-center justify-center w-6/12">
      <Calculator />
    </div>

    <div class="h-screen flex items-center justify-center w-6/12">
      <Quotation />
    </div>
  </div>
</template>
 