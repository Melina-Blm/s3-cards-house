<script setup lang="ts">
    import { supabase } from "../../supabase";
    import groupBy from "lodash/groupBy";

    const { data, error } = await supabase.from("QuartierCommune").select("*");
    if (error) console.log("n'a pas pu charger la table quartiercommune :", error);
    </script>
    
    <template>
      <section class="flex flex-col">
        <h3 class="text-2xl">Liste des quartiers</h3>
        <ul>
          <li v-for="quartierObject in (data as any[])">
            {{ quartierObject.libelle_commune }} -
            {{ quartierObject.libelle_quartier }}
          </li>
        </ul>
      </section>
    </template>