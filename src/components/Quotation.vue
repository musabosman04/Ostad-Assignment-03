<script setup>
import { ref } from 'vue';
import QuotationDetails from './QuotationDetails.vue';
const quote = ref({});

const fetchQuote = async () => {
    const response = await fetch('https://animechan.xyz/api/random');
    const data = await response.json();
    quote.value = data;
};

fetchQuote();
</script>

<template>
    <div class="w-full">

        <QuotationDetails :details="quote" />

        <button @click="fetchQuote()"
            class="mt-3 py-3 px-5 border ms-auto bg-blue-500 rounded hover:bg-blue-600 text-white">Get New Quote</button>

    </div>
</template>