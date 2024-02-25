<script setup>
defineProps({
    details: Object
})

</script>

<template>
    <h2 class="font-bold text-xl mb-3">Random Anime Quote</h2>
    <p><strong>ID:</strong> {{ details.id }}</p>
    <p><strong>Quote:</strong> {{ details.quote }}</p>
    <p><strong>Anime:</strong> {{ details.anime }}</p>
    <p><strong>Character:</strong> {{ details.character }}</p>
</template>
