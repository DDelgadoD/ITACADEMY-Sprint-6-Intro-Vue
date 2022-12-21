<template>
    <div v-for="(obj, index) in data">
        <div :class="{red: currentSentence[index], white:!currentSentence[index] }" class="border border-dark rounded-pill p-3 m-3 text-center op">
            {{ obj.sentence }}
        </div>
    </div>
</template>
<script setup>

const props = defineProps({
  data: Array,
  currentSentence: Array
});

</script>
<style scoped>
    .red{
        background-color: #ffc0cb;
        
    }

    .white{
        background-color: white;
    }

    .op{
        opacity: 80%;
    }

</style>