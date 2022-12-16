<template>
    <div v-for="sentence in data.sentences">
        <div class="border border-dark rounded-pill p-3 m-3 text-center">
            {{ sentence }}
        </div>
    </div>
</template>
<script setup>
    import data from "../data/data.json"
</script>
<style scoped>
</style>