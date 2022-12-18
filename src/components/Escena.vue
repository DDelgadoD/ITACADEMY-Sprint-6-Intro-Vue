<template>
    <div v-for="(sentence,index) in sentences">
        <div :class="{red:currentSentence[index]}" class="border border-dark rounded-pill p-3 m-3 text-center">
            {{ sentence }}
        </div>
    </div>
</template>
<script setup>

const props = defineProps({
  sentences: Array,
  currentSentence: Array
});

</script>
<style scoped>
    .red{
        background-color: #ffc0cb;
    }
</style>