<script setup lang="ts">
import { supabase } from "../supabase";
console.log("supabase :", supabase); // pour vérifier et "garder" supabase dans le code
const maisons = []; // à remplacer par l'appel à Supabase

let { data: Maison, error } = await supabase.from("Maison").select("*");
</script>

<template>
  <div>
    <h1>Page Liste Supabase</h1>
  </div>
</template>
