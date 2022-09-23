<script setup lang="ts">
import { supabase } from "../supabase";
console.log("supabase :", supabase); // pour vérifier et "garder" supabase dans le code

let { data: maison, error } = await supabase.from("Maison").select("*");
console.log("maison :", maison);
</script>

<template>
  <div>
    <h1>Page Liste Supabase</h1>
  </div>
</template>
