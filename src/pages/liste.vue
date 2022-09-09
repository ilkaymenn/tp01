<template>
  <div class="p-2">
    <h1 class="text-2xl">Page Liste</h1>
    <div v-for="maisons in maisons" :key="maisons.nom">
      <card class="w-1/2" v-bind="maisons" />
    </div>
  </div>
</template>

<script setup lang="ts">
import card from "../components/card.vue";

const maisons = [
  {
    nom: "1ère maison",
    price: 2450,
    favoris: false,
    txt: "Hopitaux",
    nbbed: 3,
    nbbath: 1,
    nbsize: "110 m²",
    img: "/public/card2.jpg",
  },
  {
    nom: "2nd maison",
    price: 6870,
    favoris: true,
    txt: "Chicago",
    nbbed: 7,
    nbbath: 3,
    nbsize: "140 m²",
    img: "/public/card3.jpg",
  },
  {
    nom: "Dernière maison",
    price: 3890,
    favoris: false,
    txt: "Bellville",
    nbbed: 4,
    nbbath: 3,
    nbsize: "90 m²",
    img: "/public/card4.jpg",
  },
];
</script>
