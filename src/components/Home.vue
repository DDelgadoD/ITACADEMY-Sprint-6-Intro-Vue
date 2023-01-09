<template >
  <div v-if="isShowed">
    <div class="flex flex-column mt-5 border border-dark mx-5 shadow-lg">
      <div class="m-5">
        A continuació podrás veure un tutorial, en el qual, mitjançant dos botons els nous usuaris poden avançar o
        retrocedir en els consells, modificant-se el text d'ajuda i la imatge de fons.
      </div>
      <div class="d-flex justify-content-center">
        <button class="btn btn-success btn-lg rounded-pill my-4 " @click="isShowed = !isShowed"> D'accord </button>
      </div>
    </div>
  </div>
  <div v-else class="background" :style="{backgroundImage: 'url(' + bgImg +')' }">
    <Botons  :currentSentence="currentSentence" @move="move" />
    <Escena :data="data" :currentSentence="currentSentence" />
  </div>
</template>

<script setup>
import Botons from './Botons.vue';
import Escena from './Escena.vue';
import data from "../data/data";
import { ref, computed} from 'vue';



const currentSentence = ref([1, 0, 0, 0]);
const isShowed = ref(true);
const move = (arr, dir=1) => dir >= 0 ?  arr.push(arr.shift()) : arr.unshift(arr.pop()); 
const bgImg = computed(() => data[currentSentence.value.findIndex(a => a==1)].img)

</script>




<style scoped>
.background {
  height: 100vh;
  width: 100vw;
  background-size:cover;
  background-position:center;
}
</style>
