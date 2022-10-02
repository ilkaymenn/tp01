<script setup lang="ts">
import { supabase } from "../supabase";

import Formulairequartier from "../components/Formulairequartier.vue";
import card from "../components/card.vue";

console.log("supabase :", supabase); // pour vérifier et "garder" supabase dans le code

let { data: quartier, error } = await supabase.from("quartier").select("*");
console.log(quartier);
</script>

<template>
  <h2 class="text-2xl font-bold text-blue-500 underline">
    Editer les quartier sur supabase
  </h2>
  <Card></Card>
  <Formulairequartier></Formulairequartier>
</template>
