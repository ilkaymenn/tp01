<script setup lang="ts">
import card from "../components/card.vue";

const objet = {
  nom: "Maison familiale",
  price: 4875,
  favoris: true,
  txt: "Beverly Springfield",
  nbbed: 8,
  nbbath: 5,
  nbsize: "120 m²",
  img: "/public/card.jpg",
};
</script>

<template>
  <div class="p-2">
    <h1 class="text-2xl font-bold text-blue-500 underline">Page Simple</h1>
    <card class="w-1/2" v-bind="objet" />
  </div>
</template>
