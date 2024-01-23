<script setup>
import { ref } from 'vue';

const compteur = ref(0);
const courses = ["pain", "chocolat"];

function increment() {
  compteur.value++;
}

</script>

<template>
  <button class="bg-red-500" @click="increment()">mon bouton</button>
  <p class="">Jai taper sur le bouton plusieurs {{ compteur }} fois sur le bouton</p>
  <p v-if="compteur > 10">
    ça fait mal
  </p>
  <p v-else>
    pas mal
  </p>

  <h1>Liste de course</h1>
  <ul>
    <li v-for="item in courses">{{ item }}</li>
  </ul>
</template>
