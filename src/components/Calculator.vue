<script setup>
import { ref } from 'vue';
const num1 = ref('');
const num2 = ref('');
const operation = ref('');
const result = ref(null);

const calculate = () => {
    switch (operation.value) {
        case '+':
            result.value = parseFloat(num1.value) + parseFloat(num2.value);
            break;
        case '-':
            result.value = parseFloat(num1.value) - parseFloat(num2.value);
            break;
        case '*':
            result.value = parseFloat(num1.value) * parseFloat(num2.value);
            break;
        case '/':
            result.value = parseFloat(num1.value) / parseFloat(num2.value);
            break;
        default:
            result.value = null;
    }
};
</script>

<template>
    <div>
        <input class="border py-[0.75rem] px-3 h-[50px] border-gray-500 focus-visible:outline-none border-e-0" type="number"
            v-model="num1" placeholder="Enter number 1">
        <input class="border py-[0.75rem] px-3 h-[50px] border-gray-500 focus-visible:outline-none border-e-0" type="number"
            v-model="num2" placeholder="Enter number 2">
        <select class="border py-[0.76rem] px-3 pe-5 h-[50px] border-gray-500 focus-visible:outline-none cursor-pointer"
            v-model="operation">
            <option value="">Select Operation</option>
            <option value="+">Addition (+)</option>
            <option value="-">Subtraction (-)</option>
            <option value="*">Multiplication (*)</option>
            <option value="/">Division (/)</option>
        </select>
        <div class=" text-end flex mt-5 items-center">
            <div v-if="result !== null">Result: <strong>{{ result }}</strong></div>
            <button @click="calculate"
                class="py-3 px-5 border ms-auto bg-blue-500 rounded hover:bg-blue-600 text-white">Calculate</button>
        </div>
    </div>
</template>