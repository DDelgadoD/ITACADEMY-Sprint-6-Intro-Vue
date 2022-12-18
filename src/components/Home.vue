<template>
  <Botons :currentSentence="currentSentence"/>
  <Escena :sentences="data.sentences" :currentSentence="currentSentence" />
</template>

<script setup>
import Botons from './Botons.vue';
import Escena from './Escena.vue';
import data from "../data/data.json";
import { ref } from 'vue';

const currentSentence = ref([1,0,0,0]);


</script>

<style scoped>

</style>
