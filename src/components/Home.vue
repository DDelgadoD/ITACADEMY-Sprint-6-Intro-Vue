<template>
  <div v-if="isShowed">
    <div class="flex flex-column mt-5 border border-dark mx-5 w-50 mx-auto shadow-lg">
      <div class="m-5">
        A continuació podrás veure un tutorial, en el qual, mitjançant dos botons els nous usuaris poden avançar o
        retrocedir en els consells, modificant-se el text d'ajuda i la imatge de fons.
      </div>
      <div class="d-flex justify-content-center">
        <button class="btn btn-success btn-lg rounded-pill my-4 " @click="isShowed = !isShowed"> D'accord </button>
      </div>
    </div>
  </div>
  <div v-else>
    <Botons :currentSentence="currentSentence" />
    <Escena :sentences="data.sentences" :currentSentence="currentSentence" />
  </div>
</template>

<script setup>
import Botons from './Botons.vue';
import Escena from './Escena.vue';
import data from "../data/data.json";
import { ref } from 'vue';

const currentSentence = ref([1, 0, 0, 0]);
const isShowed = ref(true);

</script>

<style scoped>

</style>
