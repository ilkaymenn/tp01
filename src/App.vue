<template>
  <nav class="bg-gray-300">
    <h1 class="text-3xl font-bold text-blue-400 underline">
      <Bars3Icon class="inline-block h-5 w-5 text-blue-500" />
      Agence Immobiliaire
    </h1>
    <ul>
      <li>
        <router-link class="text-black underline hover:text-blue-300" to="/">
          lien vers
          <code class="font-mono">Accueil</code>
        </router-link>
      </li>
      <li>
        <router-link
          class="text-black underline hover:text-blue-300"
          to="/simple"
        >
          <h2>lien vers Page Simple</h2>
        </router-link>
      </li>
      <li>
        <router-link
          class="text-black underline hover:text-blue-300"
          to="/liste"
        >
          <h2>lien vers Page Liste</h2>
        </router-link>
      </li>
      <li>
        <router-link
          class="text-black underline hover:text-blue-300"
          to="/liste-fetch"
        >
          <h2>lien vers Page Liste-Fetch</h2>
        </router-link>
      </li>
      <li>
        <router-link
          class="text-black underline hover:text-blue-300"
          to="/edit/new"
        >
          <h2>lien vers Page Formulaire</h2>
        </router-link>
      </li>
      <li>
        <router-link
          class="text-black underline hover:text-blue-300"
          to="/liste-supabase"
        >
          <h2>lien vers Page Supabase</h2>
        </router-link>
      </li>
      <li>
        <router-link
          class="text-black underline hover:text-blue-300"
          to="/connexion"
        >
          <h2>S'authentifier par email/mot de passe</h2>
        </router-link>
      </li>
      <li>
        <router-link
          class="text-black underline hover:text-blue-300"
          to="/Quartier"
        >
          <h2>Quatier</h2>
        </router-link>
      </li>
      <li>
        <router-link
          class="text-white underline hover:text-blue-300"
          to="/editquartier"
        >
          <h2>Edit</h2>
        </router-link>
      </li>
    </ul>
  </nav>

  <!-- Affiche les pages -->
  <Suspense>
    <router-view class="m-2 border-2 p-2" />
  </Suspense>
</template>

<script setup lang="ts">
import { Bars3Icon } from "@heroicons/vue/20/solid";
</script>
