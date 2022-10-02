<script setup lang="ts">
import { supabase } from "../supabase";

import { Disclosure, DisclosureButton, DisclosurePanel } from "@headlessui/vue";

import groupBy from "lodash/groupBy";

const { data, error } = await supabase.from("quartiercommune").select("*");
if (error) console.log("n'a pas pu charger la table quartiercommune :", error);
</script>

<template>
  <section class="flex flex-col">
    <h3 class="text-2xl font-bold text-blue-500 underline">
      Liste des quartiers
    </h3>
    <!-- <ul>
      <li v-for="Quartier in (data as any[])">
        {{ Quartier.libelle_Commune }} -
        {{ Quartier.libelle_Quartier }}
      </li>
    </ul> -->

    <Disclosure
      v-for="(tableau, libelle_Commune) in groupBy(data, 'libelle_Commune')"
      :key="libelle_Commune"
    >
      <DisclosureButton>
        {{ libelle_Commune }}
      </DisclosureButton>
      <DisclosurePanel class="">
        <ul>
          <li
            v-for="{ code_Quartier, libelle_Quartier } in tableau"
            :key="code_Quartier"
          >
            {{ libelle_Quartier }}
          </li>
        </ul>
      </DisclosurePanel>
    </Disclosure>
  </section>
</template>
