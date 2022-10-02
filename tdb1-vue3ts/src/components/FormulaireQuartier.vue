<script setup lang="ts">

import { supabase } from '@/supabase';
import {ref} from "@vue/reactivity";
import card from "@/components/card.vue";
import { useRouter } from "vue-router";

const router = useRouter ();
const quartier = ref ({});

const props = defineProps(["id"]);
if (props.id) {
    // On charge les données de la maison
    let { data, error } = await supabase
    .from("Quartier")
    .select("*")
    .eq("codeQuartier", props.id);
    if (error) console.log("n'a pas pu charger la table Quartier :", error);
    else quartier.value = (data as any[])[0];
}


async function upsertQuartier(dataForm, node) {
    const { data, error } = await supabase.from("Quartier").upsert(dataForm);
    if (error || !data) node.setErrors([error?.message])
    else {
        node.setErrors([]);
        router.push({ name: "quartier-id", params: { id: data[0].codeQuartier } });
    }
}

const { data: listeCommune, error } = await supabase
  .from("Commune")
  .select("*");
if (error) console.log("n'a pas pu charger la table Commune :", error);
// Les convertir par `map` en un tableau d'objets {value, label} pour FormKit
const optionsCommune = listeCommune?.map((Commune) => ({
  value: Commune.code_commune,
  label: Commune.libelle_commune,
}));

    </script>
    <template>
      <FormKit type="form">
        <!-- TODO -->
      </FormKit>
    </template>