<template>
    <div v-for="sentence in data.sentences">
        <div>
            {{ sentence }}
        </div>
    </div>
</template>
<script setup>
    import data from "../data/data.json"
</script>
<style scoped>
</style>