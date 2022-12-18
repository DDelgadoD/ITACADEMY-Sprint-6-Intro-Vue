<template>
    <div class="d-flex m-2">
        <button class="p-4 flex-fill" @click="move(currentSentence, 1)">Anterior</button>
        <button class="p-4 flex-fill" @click="move(currentSentence, -1)">Següent</button>
    </div>
</template>
<script setup>

const props = defineProps({
    currentSentence: Array
});

const move = (arr, dir=1) => dir >= 0 ?  arr.push(arr.shift()) : arr.unshift(arr.pop()); 

</script>
<style scoped>

</style>