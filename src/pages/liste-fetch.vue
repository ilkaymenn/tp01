<script setup lang="ts">
import card from "../components/card.vue";

const res = await fetch("/maisons.json");
const maisons = await res.json();
</script>

<template>
  <div class="p-2">
    <h1 class="text-2xl font-bold text-blue-500 underline">Page Liste Fetch</h1>
    <div v-for="maison in maisons" :key="maison.nom">
      <card class="w-1/2" v-bind="maison" />
    </div>
  </div>
</template>
