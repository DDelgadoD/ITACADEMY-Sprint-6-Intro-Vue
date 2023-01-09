<template>
    <div class="d-flex p-2">
        <button class="p-4 flex-fill" @click="$emit('move', currentSentence, 1)">Anterior</button>
        <button class="p-4 flex-fill" @click="$emit('move', currentSentence, -1)">Següent</button>
    </div>
</template>

<script setup>
    const props = defineProps({ currentSentence: Array });
    const emit = defineEmits(['move'])
</script>

<style scoped>

</style>