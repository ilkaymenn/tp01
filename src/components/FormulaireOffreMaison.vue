<script setup lang="ts">
import { ref } from "@vue/reactivity";
import Card from "./card.vue";

// On fait une variable réactive qui réference les données
// ATTENTION : faire une Ref pas une Reactive car :
// c'est l'objet qui doit être réactif, pas ses props
const maison = ref({});
</script>
<template>
  <div>
    <div class="p-2">
      <h2 class="text-2xl">Résultat (Prévisualisation)</h2>
      <!-- Optionnel on affiche les données -->
      <Card v-bind="maison" />
    </div>
    <div class="p-2">
      <!-- On passe la "ref" à FormKit -->
      <FormKit
        type="form"
        :config="{
          classes: {
            input: 'p-1 rounded border-black shadow-sm border',
            label: 'text-gray-600',
          },
        }"
        v-model="maison"
        :submit-attrs="{ classes: { input: 'bg-red-400 p-1 rounded' } }"
      >
        <FormKit name="nom" label="nom" />
        <FormKit name="price" label="prix" type="number" />
        <FormKit
          name="favoris"
          label="favoris ?"
          type="checkbox"
          wrapper-class="flex"
        />
        <FormKit name="txt" label="texte" />
        <FormKit name="img" label="image" />
        <FormKit name="nbbed" label="bed" />
        <FormKit name="nbbath" label="bath" />
        <FormKit name="nbsize" label="size" />
      </FormKit>
    </div>
  </div>
</template>
